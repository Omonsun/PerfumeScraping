# PerfumeScraping
# Web Scraping: Decant World BD Perfume Data

## Overview
This project is a web scraper that collects men's perfume data from [Decant World BD](https://decantworldbd.com/) using **Python, BeautifulSoup, and Requests**. The scraper extracts product titles and prices from multiple pages and saves them in a CSV file for further analysis.

## Features
- Scrapes **product names and prices** from multiple pages.
- Handles **pagination** to fetch all available products.
- Implements **error handling and retries** for failed requests.
- Saves data dynamically with a **timestamped CSV filename**.

## Requirements
To run this scraper, you need to install the following dependencies:

```bash
pip install requests beautifulsoup4 pandas numpy
```

## How It Works
1. **Sends an HTTP request** to the main perfume category page.
2. **Extracts product links** from the current page.
3. **Visits each product page** to fetch the name and price.
4. **Checks for pagination** and moves to the next page if available.
5. **Handles request failures** with retries to avoid crashes.
6. **Stores the extracted data** in a CSV file with a timestamp.

## Usage
Run the script using:

```bash
python scraper.py
```

This will scrape the perfume data and save it as a CSV file in the same directory.

## Output
A CSV file named `perfume_data_YYYYMMDD_HHMMSS.csv` will be generated, containing:

| Title | Price |
|--------|--------|
| Acqua DI Gio EDT | ৳ 500.00 – ৳ 2,700.00 |
| Afnan 9pm EDP | ৳ 280.00 – ৳ 1,500.00 |

## Error Handling
- If a request fails, the scraper **retries up to 3 times** before skipping the page.
- If an element is missing (e.g., price or title), it stores "N/A" instead of breaking the script.

## Notes
- This script follows **ethical scraping** principles. Ensure you comply with the website's **robots.txt** and **terms of service**.
- If the website structure changes, you may need to update the `find()` method selectors.

## License
This project is for educational purposes. Use responsibly!

