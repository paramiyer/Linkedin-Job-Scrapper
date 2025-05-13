
# LinkedIn Job Scraper (Selenium + BeautifulSoup)

This project provides a job scraping pipeline that automates the collection of job postings from LinkedIn using Selenium and BeautifulSoup. The script logs in, fetches job IDs, scrapes job descriptions, processes skills using spaCy, and saves results into structured CSV and JSON formats.

---

## 🔧 Requirements

Install Python dependencies (you may use a virtual environment):

```bash
pip install -r requirements.txt
```

You'll also need:
- Google Chrome browser
- ChromeDriver (https://chromedriver.chromium.org/) (compatible with your Chrome version)
- A file named `user_credentials.txt` placed at `../data/` containing:
  your_email@example.com
  your_password

---

## ▶️ How to Run

```bash
python scraping_linkedin.py "data scientist" "Dubai, UAE" 120 10
```

**Arguments:**
- "data scientist" → Job keyword
- "Dubai, UAE" → Location
- 120 → Sleep time (seconds) to allow the page to load
- 10 → Number of job posts to fetch

---

## 📦 Output

The script saves the following files in the `../data/` directory:
- `Job_Ids.csv` — Raw scraped job IDs
- `linkedin_jobs_scraped.csv` — Processed job data with titles, companies, text, and extracted skills
- `linkedin_jobs_scraped.json` — Same data in JSON format

---

## 🧠 Notes

- This script uses a custom spaCy pipeline (`Spacy_text_analayzer.py`) to extract skills from job descriptions.
- Ensure LinkedIn credentials and chromedriver paths are correct before execution.
- Use responsibly and respect LinkedIn's terms of service.

