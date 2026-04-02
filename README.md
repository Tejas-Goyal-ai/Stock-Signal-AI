TradeSignal — AI-Powered Stock Analysis Dashboard
A modern, real-time stock analysis web application that fetches market data, runs technical analysis, and generates trade signals for any ticker symbol.

React TypeScript Vite Tailwind CSS

Features
Ticker Lookup — Enter any stock ticker (e.g. AAPL, TSLA) to fetch live analysis
Short-Term & Long-Term Analysis — Get separate trade signals for different time horizons
Interactive Charts — Visualize price data with Recharts
Market News Feed — Stay updated with relevant market news
Animated Loading States — Multi-step analyzing graphic while the backend processes data
Dark Fintech Theme — Glassmorphic UI with a professional trading aesthetic


Tech Stack
Layer	                              Technology
Framework	                          React 18 + TypeScript 5
Build Tool	                        Vite 5
Styling	                            Tailwind CSS 3 + shadcn/ui
Charts	                            Recharts
State	                              React Query (TanStack)
Routing	                            React Router v6
Backend	                            n8n webhook (external)

Getting Started

Prerequisites
Node.js ≥ 18
npm, yarn, pnpm, or bun


Installation
# Clone the repository
git clone <your-repo-url>
cd <project-folder>

# Install dependencies
npm install

# Start the development server
npm run dev
The app will be available at http://localhost:5173.

Build for Production

npm run build
npm run preview
Project Structure
src/
├── components/
│   ├── AnalysisCard.tsx      # Displays short/long-term analysis results
│   ├── AnalyzingLoader.tsx   # Multi-step loading animation
│   ├── MarketNews.tsx        # Market news feed
│   ├── SignalCard.tsx        # Individual trade signal display
│   ├── TickerChart.tsx       # Price chart visualization
│   ├── TickerInput.tsx       # Ticker search input
│   ├── TradeResults.tsx      # Trade results container
│   ├── WebhookDataDisplay.tsx# Raw webhook data viewer
│   └── ui/                   # shadcn/ui component library
├── hooks/                    # Custom React hooks
├── lib/                      # Utilities and mock data
├── pages/
│   ├── Index.tsx             # Main dashboard page
│   └── NotFound.tsx          # 404 page
└── main.tsx                  # App entry point


Configuration

The app sends ticker data to an n8n webhook for analysis. Update the webhook URL in src/pages/Index.tsx:

const WEBHOOK_URL = "https://your-n8n-instance/webhook/your-endpoint";


Scripts

Command	                      Description
npm run dev	                  Start dev server
npm run build	                Production build
npm run preview	              Preview production build
npm run lint	                Run ESLint
npm run test	                Run tests

License
MIT
