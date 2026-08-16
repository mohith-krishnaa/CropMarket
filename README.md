# CropMarket

A browser-based farming decision-support application focused on crop prices, market comparison, weather context, farm calculations and multilingual/voice-friendly interaction.

**Live Demo:** https://cropmarketapp.netlify.app/

> **Note:** Market prices, weather information and agricultural guidance can change. Verify important information against relevant official sources before making real-world decisions.

## Overview

CropMarket is designed around a simple question:

> **Where and when should I sell my crop?**

The interface combines market-oriented calculations with contextual information such as prices, weather, crop trends, nearby markets and storage considerations.

## Features

- Home/dashboard experience
- Market views and crop search
- Price and trend presentation
- Watchlist and price-alert UI
- Weather-related information and harvest-risk messaging
- Nearby-market/location workflows
- Trip-cost and profitability calculations
- Crop calendar and storage-related tools
- Unit conversion/reference information
- Voice input and text-to-speech UI hooks
- Responsive browser interaction
- Multilingual interface support

## Architecture

```text
React UI
   │
   ├── Location / district selection
   ├── Market & crop views
   ├── Weather context
   ├── Watchlist / alerts
   ├── Trip calculator
   ├── Crop tools
   └── Voice / language UI

Single application source
        ↓
     cropmarket.jsx
```

## Tech stack

- React
- JavaScript / JSX
- React hooks
- Recharts
- Lucide React
- Browser location/voice capabilities where supported

## Running locally

The repository currently contains the application source rather than a conventional package-managed project. A generic `npm install` / `npm run build` instruction should therefore not be assumed without the corresponding package configuration.

For the quickest evaluation, use the live demo above.

## Data accuracy

Agricultural prices, weather information, government schemes and market recommendations can change over time. A displayed value does not by itself establish that the value is current or official.

Before using CropMarket for real farming decisions, verify important prices, MSP values, weather warnings and government-scheme information against the relevant official sources.

## Privacy considerations

Location and voice features can involve browser permissions. A production data layer should clearly document:

- Why location is requested
- Whether location is stored
- Whether voice/audio leaves the device
- Which external APIs receive user data
- How API keys are protected

## License

See the repository for the applicable source-code license.

## Author

**Mohith Krishnaa** — [@mohith-krishnaa](https://github.com/mohith-krishnaa)
