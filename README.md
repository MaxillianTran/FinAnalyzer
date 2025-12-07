# FinAnalyzer

A Custom GPT for stock market analysis and financial data retrieval, integrating with Yahoo Finance via RapidAPI.

## Overview

FinAnalyzer is a specialized GPT assistant that helps users analyze stock market data and retrieve real-time financial information. It integrates with Yahoo Finance through RapidAPI to provide comprehensive market data on demand.

## Features

- **Real-Time Stock Quotes**: Get current prices, volume, and market data for any stock
- **Historical Data**: Access historical price information over various time periods
- **Financial Statistics**: Retrieve comprehensive financial metrics (P/E ratio, market cap, dividend yield, etc.)
- **Stock Summaries**: Get detailed company profiles and market summaries
- **User-Initiated Only**: Data is retrieved only when you explicitly request it

## Privacy & Data Handling

### No Personal Information Storage
- The GPT author does not collect, store, or share any personal information
- No user queries or conversation history is saved
- Market data is retrieved on-demand and not stored permanently

### Third-Party Services
All financial data requests are processed through:
- **OpenAI**: Text processing and conversation management
- **RapidAPI + Yahoo Finance**: Market data retrieval

For detailed information, see [PRIVACY.md](PRIVACY.md)

## Setup Instructions

### For OpenAI Custom GPT Configuration

1. **Create a new Custom GPT** in ChatGPT
2. **Copy the instructions** from [gpt-instructions.md](gpt-instructions.md) into the GPT instructions field
3. **Set up Actions**:
   - Enable Actions in the GPT configuration
   - Import the OpenAPI schema from [openai-schema.json](openai-schema.json)
   - Configure RapidAPI authentication:
     - Sign up for [RapidAPI](https://rapidapi.com/)
     - Subscribe to [Yahoo Finance API](https://rapidapi.com/sparior/api/yahoo-finance15)
     - Add your RapidAPI key as authentication in the Actions configuration
     - Set `X-RapidAPI-Key` header with your API key
     - Set `X-RapidAPI-Host` header to `yahoo-finance15.p.rapidapi.com`

### RapidAPI Configuration

1. Create a free account at [RapidAPI](https://rapidapi.com/)
2. Subscribe to the Yahoo Finance API (free tier available)
3. Copy your API key from the RapidAPI dashboard
4. Use the API key in the Custom GPT Actions authentication configuration

## Usage Examples

Once configured, users can interact with FinAnalyzer using natural language:

- "Get the current price of Apple stock (AAPL)"
- "Show me Tesla's stock performance over the past 6 months"
- "What are Microsoft's key financial statistics?"
- "Give me a summary of Amazon's stock (AMZN)"
- "Compare the historical performance of Google and Meta"

## API Endpoints

The integration includes the following Yahoo Finance API endpoints:

### 1. Stock Quotes
- **Endpoint**: `/api/v1/markets/stock/quotes`
- **Purpose**: Real-time stock price and volume data
- **Parameters**: `ticker` (stock symbol)

### 2. Historical Data
- **Endpoint**: `/api/v1/markets/stock/history`
- **Purpose**: Historical price data over time
- **Parameters**: `symbol`, `interval` (1d/1wk/1mo), `range` (1d/5d/1mo/3mo/6mo/1y/5y/max)

### 3. Financial Statistics
- **Endpoint**: `/api/v1/markets/stock/statistics`
- **Purpose**: Comprehensive financial metrics
- **Parameters**: `ticker` (stock symbol)

### 4. Stock Summary
- **Endpoint**: `/api/v1/markets/stock/summary`
- **Purpose**: Company profile and market summary
- **Parameters**: `ticker` (stock symbol)

## Important Disclaimers

- **Not Financial Advice**: This tool provides informational data only and is not a licensed financial advisor
- **Market Data Delays**: Data may have delays depending on the source
- **No Guarantees**: Past performance does not guarantee future results
- **Consult Professionals**: Always consult qualified financial professionals for investment decisions

## Technical Details

### Architecture
- **Frontend**: OpenAI Custom GPT interface
- **Integration**: OpenAI Actions with OpenAPI 3.1.0 schema
- **Data Source**: Yahoo Finance via RapidAPI
- **Authentication**: API key-based authentication through RapidAPI

### Data Flow
1. User submits a request through ChatGPT
2. GPT processes the request using instructions
3. If market data is needed, GPT calls the appropriate Action
4. Action makes an authenticated API call to Yahoo Finance via RapidAPI
5. Data is returned and formatted for the user

## Repository Structure

```
FinAnalyzer/
├── README.md                 # This file - main documentation
├── gpt-instructions.md       # Custom GPT instructions and guidelines
├── openai-schema.json        # OpenAPI schema for Actions configuration
└── PRIVACY.md               # Privacy policy and data handling information
```

## License

This project is provided as-is for educational and informational purposes.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## Support

For questions or issues:
1. Check the documentation in this repository
2. Review the [Privacy Policy](PRIVACY.md)
3. Open an issue on GitHub

## Acknowledgments

- Market data provided by [Yahoo Finance](https://finance.yahoo.com/)
- API access through [RapidAPI](https://rapidapi.com/)
- Powered by [OpenAI](https://openai.com/)
