📌 Web Scraping Job Listings with BeautifulSoup

This project demonstrates how to scrape job postings from a mock job board using Python, Requests, and BeautifulSoup, and export the extracted data into an Excel file for structured analysis.

🚀 Features

✔ Scrapes job postings from the target webpage
✔ Extracts important fields including:

Job Title

Company

Location

Posting Date
✔ Stores results in a structured DataFrame
✔ Exports results to jobs1.xlsx
✔ Uses clean and reusable scraping logic

🛠 Tech Stack
Category	Tools Used
Language	Python
Libraries	requests, beautifulsoup4, pandas
📂 Project Structure
scraping.ipynb      # Jupyter notebook containing the implementation
jobs1.xlsx          # Output file (generated)

📥 Installation

Install dependencies:

pip install beautifulsoup4 requests pandas

🧠 How It Works

Send an HTTP GET request to fetch HTML

Parse HTML using BeautifulSoup

Find and extract job cards

Loop through each card and extract:

Title

Company

Location

Date

Store in list of dictionaries

Convert to DataFrame

Export to Excel

📌 Sample Extraction Code
job_data = []

for job_card in job_cards:
    job_data.append({
        "Title": title_element.text.strip() if title_element else "",
        "Company": company_element.text.strip() if company_element else "",
        "Location": location_element.text.strip() if location_element else "",
        "Date": time_element.get("datetime") if time_element else ""
    })

📤 Output

The script generates an Excel file:

jobs1.xlsx


Containing:

Title	Company	Location	Date
🌐 Target Website

The notebook scrapes from:

Fake Jobs board provided by RealPython (mock dataset for learning & testing)

This ensures scraping is ethical and TOS-friendly.

📄 License

This project is for educational and personal development purposes.
