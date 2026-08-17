# CropMarket 🌾

> **Smart farming decisions for crops, markets, storage and trip economics.**

CropMarket is a React + Vite decision-support prototype designed to help farmers compare market opportunities, understand price trends, estimate trip profitability, track crops, and access practical farming utilities.

> **Status:** Active prototype. Some market, weather and trend values are demonstration/fallback data and should not be treated as verified live mandi quotations.

## ✨ Features

- 🏠 **Farmer dashboard** — crop price snapshot, trend and decision guidance
- 📍 **District-aware experience** — district selection and location detection flow
- 🏪 **Market comparison** — nearby market cards and price comparisons
- 📈 **7-day trend visualization** — deterministic demo trend generation for consistent UI output
- 💰 **MSP comparison** — identifies whether a modal price is above, near or below MSP
- 🌧️ **Harvest-risk advisory** — combines price/arrival conditions with weather-risk flags
- ⭐ **Watchlist** — keep crops you want to monitor
- 🔔 **Price-alert UI** — interface foundation for future threshold notifications
- 🚜 **Trip calculator** — estimates fuel, labour, revenue, cost and net profit
- 🧮 **Farm utilities** — unit conversion, storage guidance and crop calendar
- 🌐 **Multilingual UI** — English and Hindi translations are included
- 🎤 **Voice-search UI** — browser speech-recognition integration where supported
- 📱 **Responsive UI** — designed for desktop and mobile layouts

## 🧱 Architecture

The original application had most of its logic in one large JSX file. The current refactor separates screens, data, utilities and presentation styling:

```text
src/
├── components/
│   ├── screens/
│   │   ├── HomeScreen.jsx
│   │   ├── MarketsScreen.jsx
│   │   ├── Onboarding.jsx
│   │   ├── TripScreen.jsx
│   │   ├── WatchScreen.jsx
│   │   ├── ToolsScreen.jsx
│   │   └── LangDrop.jsx
│   └── shared.jsx
├── data/
│   └── cropMarketData.js
├── utils/
│   ├── cropUtils.js
│   ├── formatters.js
│   ├── marketUtils.js
│   └── tripUtils.js
├── CropMarket.jsx
├── CropMarket.css
├── App.jsx
└── main.jsx
```

See [`docs/architecture.md`](docs/architecture.md) and [`docs/refactor-report.md`](docs/refactor-report.md) for details.

## 🛠️ Tech Stack

- React 19
- Vite 7
- JavaScript / JSX
- Recharts
- Lucide React
- ESLint
- GitHub Actions

## 🚀 Run locally

Requirements: Node.js 20+ recommended.

```bash
npm ci
npm run lint
npm run build
npm run dev
```

Then open the local Vite URL shown in the terminal.

## 🧪 Testing

The utility layer uses Node's built-in test runner, so no additional test framework is required:

```bash
npm test
```

## 🔐 Configuration

There are currently no required secrets for the demo build.

If a future live-data service needs credentials, use environment variables and never commit `.env` files. Start from [`.env.example`](.env.example).

## 🤖 CI

GitHub Actions runs linting, unit tests and the production build on pushes and pull requests. See [`.github/workflows/ci.yml`](.github/workflows/ci.yml).

## ⚠️ Data disclaimer

The current prototype contains seeded/demo datasets and fallback market entries. A generated market name or price does **not** imply that it is a verified live market quotation.

The next production step is a dedicated service/data layer for authenticated live sources, schema validation, caching, retries and explicit offline states.

## 🗺️ Roadmap

### Near term
- [x] Split the monolithic application into feature modules
- [x] Extract data and business utilities
- [x] Add deterministic trend generation
- [x] Add lint/build CI
- [x] Add utility tests
- [ ] Add live market-data service abstraction
- [ ] Add API response validation
- [ ] Add persistent watchlist storage
- [ ] Implement real price alerts

### Later
- Historical price analytics
- Offline-first caching
- Local-language voice workflows
- Farmer notification service
- Crop/market personalization

## 📄 License

MIT License.
