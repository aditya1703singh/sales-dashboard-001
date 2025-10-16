# Sales Summary SPA

## Overview
This single-page application reads a CSV file (data.csv), sums the values in the Sales column, and displays the total inside the #total-sales element. It is designed to be lightweight, dependency-free, and easy to host statically.

The page title is automatically set to "Sales Summary ${seed}" when a global seed value is provided (e.g., via window.seed or a seed query parameter).

## Setup
- Files:
  - index.html
  - data.csv (must reside in the same directory as index.html)

No build step is required. Any static file server or direct file opening in a modern browser will work.

## Usage
1. Place data.csv next to index.html. Example content:
   Product,Sales
   Product A,100
   Product B,300

2. Open index.html in a browser:
   - The app fetches data.csv, sums the Sales column, and writes the result into the #total-sales element.

3. Optional: Provide a seed to match the desired title format:
   - If your environment defines window.seed, the title will be set automatically.
   - Alternatively, append ?seed=YOUR_VALUE to the URL, e.g.:
     index.html?seed=12345

## License
MIT License

Copyright (c) 2025 Sales Summary SPA Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.