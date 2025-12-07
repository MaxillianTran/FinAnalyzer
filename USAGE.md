# FinAnalyzer Usage Guide

This guide provides examples and best practices for using FinAnalyzer to retrieve and analyze stock market data.

## Quick Start

FinAnalyzer responds to natural language requests about stock market data. Simply ask questions about stocks, and it will retrieve the relevant information from Yahoo Finance.

## Basic Queries

### Getting Current Stock Prices

**Example Requests:**
- "What's the current price of Apple stock?"
- "Get me the latest quote for TSLA"
- "How is Microsoft (MSFT) trading today?"
- "Show me the current price of Amazon"

**What You'll Get:**
- Current stock price
- Trading volume
- Price change and percentage change
- Day's high and low
- Opening price

### Historical Stock Data

**Example Requests:**
- "Show me Apple's stock performance over the past month"
- "Get Tesla's historical data for the last 6 months"
- "How has Microsoft performed over the past year?"
- "Show me Amazon's price history for the last 3 months"

**What You'll Get:**
- Historical price data points
- Date ranges you specified
- Opening, closing, high, and low prices
- Trading volumes over time

### Financial Statistics

**Example Requests:**
- "What are Apple's key financial statistics?"
- "Show me Tesla's financial metrics"
- "Get the P/E ratio and market cap for Microsoft"
- "What's Amazon's dividend yield?"

**What You'll Get:**
- Market capitalization
- P/E ratio (Price-to-Earnings)
- EPS (Earnings Per Share)
- Dividend yield
- Beta
- 52-week high/low
- Other key financial metrics

### Company Summaries

**Example Requests:**
- "Give me a summary of Apple stock"
- "Tell me about Tesla as a company"
- "What does Microsoft do?"
- "Summarize Google's stock (GOOGL)"

**What You'll Get:**
- Company profile
- Business description
- Key statistics
- Current market data
- Sector and industry information

## Advanced Queries

### Comparing Multiple Stocks

**Example Requests:**
- "Compare Apple and Microsoft stocks"
- "How do Tesla and Ford compare?"
- "Show me the difference between Google and Meta"
- "Compare the performance of Netflix, Disney, and Amazon"

**Tips:**
- Request specific metrics for clearer comparisons
- Specify time frames for historical comparisons
- Ask for specific financial metrics to compare

### Time-Specific Analysis

**Example Requests:**
- "How did Apple perform in the last week?"
- "Show me Tesla's 5-year performance"
- "What's Amazon's stock movement over the last quarter?"
- "Get Microsoft's daily data for the past 5 days"

**Available Time Ranges:**
- 1 day (1d)
- 5 days (5d)
- 1 month (1mo)
- 3 months (3mo)
- 6 months (6mo)
- 1 year (1y)
- 5 years (5y)
- Maximum available (max)

### Sector and Industry Analysis

**Example Requests:**
- "Show me major tech stocks"
- "How are automotive stocks performing?"
- "Compare stocks in the semiconductor industry"
- "What are the top gainers in the energy sector?"

**Note:** For sector-wide queries, you may need to specify individual ticker symbols.

## Best Practices

### 1. Use Standard Ticker Symbols
- Use official stock ticker symbols (e.g., AAPL, TSLA, MSFT)
- US market stocks work best
- You can ask about the ticker symbol if you're unsure

### 2. Be Specific in Your Requests
- **Less Specific:** "Tell me about Apple"
- **More Specific:** "Get Apple's current stock price and P/E ratio"

### 3. Specify Time Frames
- **Less Clear:** "Show me Tesla's performance"
- **More Clear:** "Show me Tesla's stock performance over the past 6 months"

### 4. Ask Follow-Up Questions
- Build on previous queries for deeper analysis
- Request specific metrics after getting a summary
- Ask for comparisons based on initial data

### 5. Request Clarification
- If you're unsure about a metric, ask what it means
- Request explanations of financial terms
- Ask for context on unusual market movements

## Understanding the Data

### Price Metrics
- **Current Price**: Latest traded price
- **Open**: Price at market open
- **Close**: Price at market close (previous day)
- **High/Low**: Highest and lowest prices during the trading day
- **52-Week High/Low**: Highest and lowest prices over the past year

### Volume Metrics
- **Volume**: Number of shares traded
- **Average Volume**: Typical daily trading volume
- High volume can indicate strong interest or volatility

### Financial Metrics
- **Market Cap**: Total value of all shares (Price × Shares Outstanding)
- **P/E Ratio**: Price-to-Earnings ratio (valuation metric)
- **EPS**: Earnings Per Share (profitability metric)
- **Beta**: Volatility compared to the market
- **Dividend Yield**: Annual dividend as percentage of stock price

## Sample Conversations

### Example 1: Quick Price Check
**You:** "What's Tesla's current price?"
**FinAnalyzer:** [Retrieves and displays current TSLA quote with price, change, and volume]

### Example 2: Detailed Analysis
**You:** "I want to learn about Microsoft stock"
**FinAnalyzer:** [Provides company summary and key metrics]
**You:** "What's their P/E ratio?"
**FinAnalyzer:** [Shows P/E ratio and explains what it means]
**You:** "How has it performed over the past year?"
**FinAnalyzer:** [Retrieves and analyzes 1-year historical data]

### Example 3: Comparison
**You:** "Compare Apple and Samsung stocks"
**FinAnalyzer:** [Note: Samsung trades on different exchanges, so might request clarification]
**You:** "Compare Apple (AAPL) and Microsoft (MSFT)"
**FinAnalyzer:** [Retrieves data for both and provides comparison]

## Common Ticker Symbols

### Technology
- AAPL - Apple Inc.
- MSFT - Microsoft Corporation
- GOOGL - Alphabet Inc. (Google)
- META - Meta Platforms (Facebook)
- AMZN - Amazon.com Inc.
- TSLA - Tesla Inc.
- NVDA - NVIDIA Corporation
- NFLX - Netflix Inc.

### Finance
- JPM - JPMorgan Chase
- BAC - Bank of America
- GS - Goldman Sachs
- V - Visa Inc.
- MA - Mastercard

### Other Major Stocks
- WMT - Walmart
- DIS - Disney
- KO - Coca-Cola
- PG - Procter & Gamble
- JNJ - Johnson & Johnson

## Limitations

### What FinAnalyzer CAN Do
✅ Retrieve current stock quotes
✅ Get historical price data
✅ Provide financial statistics
✅ Explain financial metrics
✅ Compare stocks based on data
✅ Show market trends

### What FinAnalyzer CANNOT Do
❌ Predict future stock prices
❌ Provide personalized investment advice
❌ Execute trades
❌ Access your portfolio
❌ Guarantee data accuracy
❌ Replace professional financial advisors

## Tips for Best Results

1. **Start Simple**: Begin with basic queries, then ask follow-up questions
2. **Use Official Symbols**: Use proper ticker symbols for accurate results
3. **Specify Details**: Include time frames, specific metrics, or comparison points
4. **Verify Important Data**: Cross-check critical information with official sources
5. **Ask for Explanations**: Don't hesitate to ask what financial terms mean
6. **Understand Delays**: Market data may have slight delays
7. **Context Matters**: Provide context for better analysis

## Privacy Reminder

- FinAnalyzer does not store your queries or personal information
- Data is retrieved only when you request it
- All processing is handled by OpenAI and RapidAPI
- See [PRIVACY.md](PRIVACY.md) for full details

## Important Disclaimer

FinAnalyzer provides informational data only and is **NOT** financial advice. Always:
- Consult with qualified financial professionals
- Do your own research
- Understand the risks of investing
- Make informed decisions based on multiple sources

## Need Help?

- Review this guide for usage examples
- Check [README.md](README.md) for setup information
- See [SETUP.md](SETUP.md) for configuration details
- Refer to [PRIVACY.md](PRIVACY.md) for privacy information
- Review [TERMS.md](TERMS.md) for terms of service

## Feedback

Your feedback helps improve FinAnalyzer. If you encounter issues or have suggestions:
- Open an issue on the GitHub repository
- Provide specific examples of what worked or didn't work
- Suggest new features or improvements
