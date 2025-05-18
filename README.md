📘 Notebook Description: scraping avtoelon.uz.ipynb
This Jupyter Notebook is a web scraper for the Avtoelon.uz website, which is one of the most popular car selling dilership in Uzbekistan. The scraper is implemented using Selenium WebDriver and includes logic for:

🔧 Main Features:
Automated Browser Navigation with Selenium

Uses a headless Chrome browser to simulate a real user.

Opens the Avtoelon.uz search result pages for cars.

Pagination Support

Loops through multiple listing pages by clicking the "next" button until the last page is reached.

Car Links Collection

Extracts all individual car listing URLs from each search result page.

Stores the collected URLs in a list called car_links.

Detailed Car Info Scraping

Visits each car listing URL.

Extracts key data fields such as:

Title

Price

Location

Description

Characteristics (e.g. year, engine size, fuel type)

Seller phone number (with retries)

Uses safe_get_text utility function to avoid crashes due to missing elements.

Phone Number Retry Logic

If a phone number is not successfully retrieved, the scraper retries up to 5 times.

Failed URLs are stored in unread_urls and retried later after all others are processed.

Structured Data Storage

Compiles all scraped data into a list of dictionaries for each car.

Includes timestamp and status for reliability.

Final Export

Saves the results into a CSV or another format (not shown in preview but typically included in such scrapers).

🧠 Code Structure Highlights:
Modular design with:

get_car_links(): Collects all listing URLs from paginated pages.

scrape_car_data(): Extracts all info from a single car page.

Use of explicit waits and try-except blocks for robust scraping.

Use of classes and reusable functions to improve organization and maintainability.

✅ Summary:
This notebook automates the extraction of detailed car listings from Avtoelon.uz with robust handling for dynamic content and missing data. It is well-suited for building datasets for car price analysis, dealership comparisons, or regional vehicle trends.

Code for cleaning this data will be provided soon using pandas and numpy
