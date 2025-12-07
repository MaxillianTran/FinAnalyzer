# Configuration Guide for FinAnalyzer Custom GPT

This guide provides step-by-step instructions for configuring the FinAnalyzer Custom GPT in OpenAI's ChatGPT platform.

## Prerequisites

1. ChatGPT Plus or Enterprise subscription (required for Custom GPTs)
2. RapidAPI account (free tier available)
3. Yahoo Finance API subscription through RapidAPI

## Step 1: RapidAPI Setup

### 1.1 Create RapidAPI Account
1. Visit [RapidAPI](https://rapidapi.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

### 1.2 Subscribe to Yahoo Finance API
1. Search for "Yahoo Finance" in the RapidAPI marketplace
2. Select the "Yahoo Finance15" API (or similar Yahoo Finance API)
3. Choose a pricing plan (free tier available for testing)
4. Click "Subscribe"
5. Note your API key from the API dashboard

### 1.3 Test Your API Access
1. In RapidAPI, navigate to the API endpoints
2. Try the "Test Endpoint" feature to verify access
3. Ensure you can successfully retrieve stock data

## Step 2: Create Custom GPT

### 2.1 Access GPT Builder
1. Log in to ChatGPT (Plus or Enterprise account required)
2. Click your profile icon
3. Select "My GPTs"
4. Click "Create a GPT"

### 2.2 Configure Basic Settings
1. **Name**: FinAnalyzer
2. **Description**: Stock market analysis assistant with real-time data from Yahoo Finance
3. **Icon**: Upload or generate an icon related to finance/stocks
4. **Conversation Starters**: Add examples like:
   - "Get the current price of AAPL"
   - "Show me Tesla's stock performance"
   - "What are Microsoft's key statistics?"
   - "Compare Google and Amazon stocks"

## Step 3: Add Instructions

1. Click on the "Configure" tab
2. In the "Instructions" field, copy and paste the entire content from `gpt-instructions.md`
3. Review the instructions to ensure they align with your needs
4. You can customize the guidelines if needed

## Step 4: Configure Actions

### 4.1 Enable Actions
1. Scroll down to the "Actions" section
2. Click "Create new action"

### 4.2 Import OpenAPI Schema
1. Copy the entire content from `openai-schema.json`
2. Paste it into the Schema field
3. The system will automatically parse the schema and show available endpoints

### 4.3 Configure Authentication
1. In the Actions section, click "Authentication"
2. Select "API Key" as the authentication type
3. Choose "Custom" header authentication
4. Add two headers:

   **Header 1:**
   - Name: `X-RapidAPI-Key`
   - Value: [Your RapidAPI API Key]
   
   **Header 2:**
   - Name: `X-RapidAPI-Host`
   - Value: `yahoo-finance15.p.rapidapi.com`

### 4.4 Privacy Settings
1. Set the appropriate privacy level for your GPT:
   - "Only me" for personal use
   - "Anyone with a link" for sharing
   - "Public" for GPT store (if applicable)

## Step 5: Test the Configuration

### 5.1 Basic Testing
1. Click "Preview" or save the GPT
2. Try a simple query: "Get the current price of Apple stock (AAPL)"
3. Verify that the GPT:
   - Understands the request
   - Calls the appropriate Action
   - Returns formatted stock data

### 5.2 Test Each Endpoint
Test all available endpoints:

1. **Stock Quote**: "Get the current price of TSLA"
2. **Historical Data**: "Show me Microsoft's stock history over the past month"
3. **Statistics**: "What are Amazon's financial statistics?"
4. **Summary**: "Give me a summary of Google's stock"

### 5.3 Error Handling
Test error scenarios:
1. Invalid ticker symbol: "Get the price of INVALIDTICKER"
2. Verify graceful error messages are displayed

## Step 6: Final Configuration

### 6.1 Capabilities Settings
Configure the following capabilities as needed:
- **Web Browsing**: Optional (can be disabled if only using API data)
- **DALL·E Image Generation**: Optional (can be disabled)
- **Code Interpreter**: Optional (can be useful for data analysis)

### 6.2 Additional Context
You can optionally upload the following files as knowledge:
- `PRIVACY.md` - Privacy policy reference
- Additional documentation or guidelines

## Step 7: Save and Publish

1. Review all settings one final time
2. Click "Save" or "Update" to save your GPT
3. If publishing:
   - Ensure compliance with OpenAI's usage policies
   - Include appropriate disclaimers
   - Set proper privacy settings

## Troubleshooting

### Common Issues

**Issue**: Actions not working
- **Solution**: Verify RapidAPI key is correct and API subscription is active
- **Solution**: Check that header names exactly match: `X-RapidAPI-Key` and `X-RapidAPI-Host`

**Issue**: No data returned
- **Solution**: Ensure ticker symbols are valid (use standard US stock symbols)
- **Solution**: Check RapidAPI dashboard for API usage limits

**Issue**: Authentication errors
- **Solution**: Verify API key has not expired
- **Solution**: Ensure Yahoo Finance API subscription is active

**Issue**: Rate limiting
- **Solution**: Check your RapidAPI plan limits
- **Solution**: Consider upgrading plan if needed

## Best Practices

1. **Test Incrementally**: Test each endpoint individually before full deployment
2. **Monitor Usage**: Regularly check RapidAPI dashboard for usage stats
3. **Update Instructions**: Keep instructions updated based on user feedback
4. **Privacy Compliance**: Ensure you comply with OpenAI's policies and data regulations
5. **User Education**: Make sure users understand this is informational data, not financial advice

## Maintenance

### Regular Checks
- Monitor RapidAPI subscription status
- Verify API endpoints are still functional
- Update schema if Yahoo Finance API changes
- Review and update instructions as needed

### Updates
When Yahoo Finance API or RapidAPI changes:
1. Update `openai-schema.json` with new endpoints/parameters
2. Update `gpt-instructions.md` if functionality changes
3. Re-import schema in Actions configuration
4. Test all endpoints again

## Security Notes

- **Never share your RapidAPI key** publicly
- Keep API credentials secure in OpenAI's Actions configuration
- Use the minimum required API permissions
- Regularly rotate API keys for security
- Monitor for unusual API usage patterns

## Support Resources

- [OpenAI Custom GPTs Documentation](https://help.openai.com/en/articles/8554397-creating-a-gpt)
- [RapidAPI Documentation](https://docs.rapidapi.com/)
- [Yahoo Finance API Documentation](https://rapidapi.com/sparior/api/yahoo-finance15)
- This repository's [README.md](README.md) and [PRIVACY.md](PRIVACY.md)

## Next Steps

After successful configuration:
1. Share the GPT with intended users
2. Gather feedback on functionality
3. Monitor usage and performance
4. Iterate on instructions based on user needs
5. Stay updated with API changes and OpenAI platform updates
