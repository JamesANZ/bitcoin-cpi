# Bitcoin vs CPI Inflation Tracker

A modern web application that compares US Consumer Price Index (CPI) inflation with Bitcoin's price performance and traditional asset price inflation over the past year.

## Features

- **Real-time Data**: Fetches current CPI inflation data, Bitcoin price data, and asset price data from reliable APIs
- **Asset Price Inflation Index**: Tracks the weighted performance of major US asset classes (S&P 500, Real Estate, Gold)
- **Multiple Comparisons**: Compares Bitcoin against both CPI inflation and traditional asset performance
- **Beautiful UI**: Modern, responsive design with gradient backgrounds and smooth animations
- **Multiple Data Sources**: Tries multiple APIs for data to ensure reliability
- **Error Handling**: Graceful fallback when APIs are unavailable
- **Mobile Responsive**: Works perfectly on desktop and mobile devices

## How It Works

The application calculates:

1. **US CPI Inflation (Annual)**: Current annual inflation rate
2. **Bitcoin Price Change (Annual)**: Bitcoin's price appreciation/depreciation over the past year
3. **Asset Price Inflation (Annual)**: Weighted average of major asset classes:
   - S&P 500 (60% weight)
   - US Real Estate (30% weight)
   - Gold (10% weight)
4. **CPI in Bitcoin Terms**: Inflation adjusted for Bitcoin's performance (CPI - Bitcoin Return)
5. **Bitcoin vs Asset Inflation**: Bitcoin's performance compared to traditional assets (Bitcoin Return - Asset Inflation)

## Asset Classes Tracked

- **S&P 500**: Major US stock market index
- **Real Estate**: US housing market (Case-Shiller index)
- **Gold**: Precious metal prices
- **Bitcoin**: Cryptocurrency performance

## Data Sources

- **CPI Data**: Multiple sources including API Ninjas and Federal Reserve Economic Data (FRED)
- **Bitcoin Data**: CoinGecko API for historical Bitcoin prices
- **Asset Data**: Currently using estimated values based on recent market performance
  - S&P 500: Estimated annual return (~12.5%)
  - Real Estate: Estimated Case-Shiller data (~5.2%)
  - Gold: Estimated annual return (~8.1%)

_Note: For production use, consider integrating with paid APIs like Alpha Vantage, Yahoo Finance, or official data sources for real-time asset prices._

## Usage

1. Open `index.html` in your web browser
2. The application will automatically fetch and display the latest data
3. Data is updated in real-time when the page loads
4. Compare Bitcoin's performance against both consumer inflation and asset inflation

## Technical Details

- **Frontend**: Vanilla HTML, CSS, and JavaScript
- **File Structure**:
  - `index.html` - Main HTML structure
  - `styles.css` - All styling and responsive design
  - `README.md` - Documentation
- **No Dependencies**: No external frameworks or libraries required
- **APIs Used**:
  - CoinGecko API (Bitcoin prices)
  - API Ninjas (CPI data)
  - FRED API (backup CPI data)

## Local Development

To run locally:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## API Keys

The application includes a demo API key for API Ninjas. For production use, you should:

1. Register for your own API key at [API Ninjas](https://api-ninjas.com/)
2. Replace the API key in the JavaScript code
3. Consider implementing rate limiting and error handling

## License

MIT License - see LICENSE file for details.

## Contributing

Feel free to submit issues and enhancement requests!
