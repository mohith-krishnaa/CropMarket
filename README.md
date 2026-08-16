# CropMarket

A browser-based farming decision-support prototype focused on crop prices, market comparison, weather context, farm calculations and multilingual/voice-friendly interaction.

**Live demo:** https://cropmarketapp.netlify.app/

> **Status:** Prototype / single-file React application. Verify external data integrations and production deployment before treating displayed information as authoritative.

## Overview

CropMarket is designed around a simple question:

> **Where and when should I sell my crop?**

The interface combines market-oriented calculations with contextual information such as prices, weather, crop trends, nearby markets and storage considerations.

The current repository is unusually small: the main application is contained in `cropmarket.jsx`. fileciteturn27file0

## Current application capabilities

The source implements a multilingual interface with English, Hindi and additional language strings, plus farmer-oriented views and tools including:

- Home/dashboard experience
- Market views and crop search
- Price/trend presentation
- Watchlist and price-alert UI
- Weather-related information and harvest-risk messaging
- Nearby-market/location workflows
- Trip-cost and profitability calculations
- Crop calendar and storage-related tools
- Unit conversion/reference information
- Voice input and text-to-speech UI hooks
- Responsive, browser-oriented interaction

The repository should be treated as a **frontend prototype** rather than a verified agricultural data platform until each external data source is confirmed in the current implementation.

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

Based on the current source:

- React
- JavaScript / JSX
- React hooks (`useState`, `useEffect`, `useRef`, `useCallback`)
- Recharts
- Lucide React
- Browser location/voice capabilities where supported

The repository currently does **not** contain a conventional `package.json`, build configuration, or `.env.example` alongside the JSX source. fileciteturn27file0

## Running the project

The repository currently contains the application source rather than a complete package-managed project. That means a generic `npm install` / `npm run build` instruction would be misleading.

To turn this into a conventional runnable React project, the next engineering step is to add a package manifest and build setup (for example Vite), then define the required dependencies and scripts.

## Data accuracy

Agricultural prices, weather information, government schemes and market recommendations can change over time. A UI displaying a value does not by itself establish that the value is current or official.

Before using CropMarket for real farming decisions, verify important prices, MSP values, weather warnings and government-scheme information against the relevant official sources.

## Security & privacy considerations

Location and voice features can involve sensitive browser permissions. A production version should clearly explain:

- Why location is requested
- Whether location is stored
- Whether voice/audio leaves the device
- Which external APIs receive user data
- How API keys are protected

API keys should never be embedded in a public frontend when the provider requires secret credentials.

## Roadmap

- Convert the prototype into a standard React/Vite project
- Separate UI, data, calculations and configuration into modules
- Add automated tests for financial/market calculations
- Add a documented data-source layer
- Add proper environment-variable handling
- Add loading/error/empty states for external data
- Add source timestamps to market and weather information
- Add accessibility testing
- Add CI/build validation
- Add an explicit privacy model for location and voice features

## License

See the repository for the applicable source-code license.

## Author

**Mohith Krishnaa** — [@mohith-krishnaa](https://github.com/mohith-krishnaa)
