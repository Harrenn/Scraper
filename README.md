# Web Scraping Script

This script is designed to scrape Instagram links, email links, and usernames from a list of URLs. It uses Selenium for web automation, BeautifulSoup for parsing HTML, and pandas for data manipulation and exporting to Excel. The script also utilizes multiprocessing to speed up the scraping process by processing multiple URLs simultaneously.

## Dependencies

- Selenium
- BeautifulSoup
- pandas
- multiprocessing

You can install these packages using pip:

```bash
pip install selenium beautifulsoup4 pandas
```

You'll also need to have the Chrome WebDriver installed and in your system's PATH.

## How It Works

The script reads a list of URLs from a text file, then uses Selenium to load each URL and BeautifulSoup to parse the HTML content. It looks for Instagram links, email links, and usernames in the HTML and stores them in a dictionary.

The script prioritizes Instagram links without 'www' and email links with the domain '@moxymgt.com'. If no such links are found, it falls back to any Instagram or email link.

The script uses multiprocessing to process multiple URLs at the same time, which can significantly speed up the scraping process if you're dealing with a large number of URLs.

After all URLs have been processed, the script converts the list of dictionaries to a pandas DataFrame and writes it to an Excel file.

## Usage

To use the script, simply run it with Python:

```bash
python scrape.py
```

Make sure to replace 'urls.txt' with the path to your text file containing the URLs to scrape, and 'output.xlsx' with the path where you want to save the Excel file.

The script will print the progress for each URL processed as a percentage.

Please note that web scraping can be resource-intensive, and running too many processes at once might slow down your computer or cause your script to crash. You might need to adjust the number of processes based on the capabilities of your machine.

Also, please be aware that some websites may have restrictions or bans on web scraping or on making too many requests in a short period of time. Always make sure to respect the website's `robots.txt` file and terms of service.

## License

This project is licensed under the terms of the MIT license. 
