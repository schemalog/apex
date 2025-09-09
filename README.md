# Apex Schema Log

Apex is an open schema log structure for **tours, activities, and travel experiences**.  
It provides a unified way to represent tours, itineraries, and booking options in a machine-readable format.

## Why Tour Schema?

Tour data is scattered across booking platforms. Reviews are fragmented. Tour Schema provides:

- Unified **tour schema**: define your tour once, reference it across platforms.
- Cross-platform reviews: aggregate feedback from OTAs (Viator, GetYourGuide, Klook, TripAdvisor, TourHubAsia, etc.).
- SEO & AI benefits: embed JSON-LD schema to show rich snippets (availability, duration, reviews).
- Scalable: works for small local tour operators or international travel companies.

## Example Tour Entry

```json
{
  "@context": "https://schema.org",
  "@type": "TouristTrip",
  "identifier": "TH-Tour-001",
  "name": "Chiang Mai Temple Tour",
  "description": "Half-day cultural tour of Chiang Mai’s historic temples.",
  "touristType": "Cultural",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "THB",
    "price": "1200",
    "url": "https://tourhubasiaexample.com/tour/chiang-mai-temples"
  }
}
{
  "@context": "https://schema.org",
  "@type": "AggregateRating",
  "itemReviewed": "TH-Tour-001",
  "ratingValue": "4.8",
  "reviewCount": 57,
  "source": ["TripAdvisor", "GetYourGuide"]
}
```

## Usage

- Drop logs into your tour site pages as JSON-LD.
- Aggregate reviews from booking platforms.
- Publish schema logs into /logs for indexing.

## Roadmap

- Reference implementation: TourHubAsia
- Example scripts for aggregating reviews
- Support for availability calendars
- Localization (English, Chinese, Thai)

## License

MIT License. Free to use, extend, or embed.
