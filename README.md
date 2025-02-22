# Data Science Job Scraper

This project is a web scraper that collects data science job listings from **Wuzzuf** and saves them into a CSV file. It extracts key details like job title, job link, job location, salary, required skills, and company name.

---

## Features

- Scrapes multiple pages of job listings.
- Filters jobs related to "data" in the job title.
- Extracts detailed information using Selenium and BeautifulSoup.
- Saves the extracted data into a CSV file (`jobs.csv` and `data_science_jobs.csv`).

---

## Requirements

Make sure to have the following installed:

- Python 3.x
- `beautifulsoup4`
- `requests`
- `selenium`
- `pandas`
- Google Chrome browser
- ChromeDriver (Ensure it's compatible with your Chrome version)

---

## Installation

1. Clone the repository:

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Download [ChromeDriver](https://chromedriver.chromium.org/downloads) and place it in a directory accessible by your system's PATH.

---

## Usage

1. Update the `pages` list to define the range of pages to scrape:

    ```python
    pages = [f"https://wuzzuf.net/search/jobs/?a=navbl&q=data%20science%20jobs&start={i}" for i in range(0, 55)]
    ```

2. Run the script:

    ```bash
    python job_scraper.py
    ```

3. The script will:

    - Scrape job listings from each page.
    - Extract job title, job link, job location, salary, required skills, and company name.
    - Save the data in `jobs.csv`.
    - Convert the data into another CSV file named `data_science_jobs.csv`.

---

## Output

Two CSV files will be generated:
- `jobs.csv`: Contains all the extracted job data.
- `data_science_jobs.csv`: A cleaned and organized version of the job data.

---

## Example Data

Sample of the data saved in `data_science_jobs.csv`:

| Job Title | Job Link | Job Location | Salary | Skills Required | Company Name |
|-----------|----------|--------------|--------|-----------------|--------------|
| Data Scientist | [Link](#) | Cairo, Egypt | 10,000 EGP | Python, Machine Learning | Example Corp |

---

## Error Handling

If an error occurs while processing a job listing, the script will:
- Print an error message with the exception details.
- Continue to the next job listing without stopping.

---

## Notes

- This scraper uses Selenium in headless mode to navigate job links and extract additional information.
- Ensure that the ChromeDriver version matches your installed Chrome browser version.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Selenium](https://www.selenium.dev/documentation/)
- [Pandas](https://pandas.pydata.org/)

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

---

## Contact

For questions or support, feel free to contact me through GitHub or email.
