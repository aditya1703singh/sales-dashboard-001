# Sales Dashboard

## Overview
A lightweight sales dashboard that showcases product sales in a responsive Bootstrap table and provides:
- A currency selector (#currency-picker) that converts and updates prices/totals using rates.json.
- A region filter (#region-filter) that recalculates totals by region and sets the data-region attribute on the #total-sales element.
- A clear grand total in the table footer and a sticky summary card with overall total sales.

The app uses client-side JavaScript only and requires no backend.

## Setup
1. Place the following files in the same directory:
   - index.html
   - rates.json (example provided below)
2. Run a local HTTP server to allow the page to fetch rates.json:
   - Python: python3 -m http.server 8080
   - Node (http-server): npx http-server -p 8080
3. Open http://localhost:8080 in your browser.

Example rates.json:
{
  "USD": 1.0,
  "EUR": 0.95,
  "IN": 83.5
}

Notes:
- The app will gracefully fall back to default rates if rates.json cannot be loaded.
- Currency code IN is formatted as INR (₹) in the UI.

## Usage
- Region filter:
  - Use the Region dropdown to switch between All, Americas, EMEA, and APAC.
  - The table recalculates units and revenue per product for the selected region.
  - The total summary (#total-sales) is updated and tagged with data-region="<SelectedRegion>".
- Currency selector:
  - Use the Currency dropdown to switch between USD, EUR, and INR (IN).
  - Unit prices, per-product revenues, the grand total row, and the top total sales summary update immediately with the selected currency.
- Table:
  - Table id: #product-sales.
  - Columns: Product, Unit Price, Units Sold (contextual to region), Revenue.
  - The footer shows the grand total, which matches the sticky summary’s total.

## Improvements in Round 2
In this iteration, the following enhancements were implemented:
- Added a responsive Bootstrap sales table (#product-sales) with accurate per-row revenues and a grand total.
- Introduced a currency selector (#currency-picker) that fetches conversion rates from rates.json and updates all monetary values across the page.
- Implemented a region filter (#region-filter) that recalculates totals for the selected region and sets the data-region attribute on #total-sales for easy programmatic verification.
- Improved UX with a sticky total summary card, accessible labels, and robust fallback behavior if rate loading fails.

## License
MIT License

Copyright (c) 2025 Sales Dashboard Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.