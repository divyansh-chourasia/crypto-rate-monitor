# Crypto rate monitor

A React page for coin prices. The screen calls itself Xcrypto. A running copy is at https://crypto-rate-monitor.netlify.app/.

The header links to Home, Exchanges, and Coins. Home is a grayscale bitcoin image that bobs, with the word Xcrypto under it. The footer shows a short line about a cheap crypto trading app in India, and a photo labeled Our Founder.

Coins and Exchanges read CoinGecko. The base URL is `server` in `src/index.js`. A failed request shows a fixed error at the bottom of the screen. While a request is in flight, the page is a spinner.

Coins lists one page of markets as cards: image, symbol, name, and price. A card opens `/coin/:id`. The currency radios are INR, USD, and EUR, and INR is selected first. Under the cards are 132 page buttons. Changing page or currency loads that page again.

A coin page draws a line chart, then the same currency radios. The range buttons are 24h, 7d, 14d, 30d, 60d, 200d, 1y, and max. The 1y button asks for 365 days. The 24h chart labels are times. The other ranges use dates. Under the chart: last updated time, image, name, price, 24h change, market-cap rank, the 24h low and high, max supply, circulating supply, market cap, all-time low, and all-time high. The range bar is drawn at the midpoint.

Exchanges loads the exchange list once. Each card shows the trust-score rank, the name, and the image, and links to that exchange's own site.

## Run

From this folder:

```bash
npm install
npm start
```

The dev server listens on port 3000 and prints the local address.
