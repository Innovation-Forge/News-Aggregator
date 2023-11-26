# RSS Feed Aggregator

## Introduction
The RSS Feed Aggregator is a Python script that aggregates news articles from multiple RSS feeds, stores them in a local SQLite database, and exports them to an Excel spreadsheet. It is designed to help users keep track of the latest news articles from their favorite news sources in an organized manner.

## Features
- **RSS Feed Parsing**: Fetches and parses multiple RSS feeds using `feedparser`.
- **Database Storage**: Stores articles in a SQLite database to prevent duplicates and maintain a history of fetched articles.
- **Excel Export**: Exports stored articles to an Excel spreadsheet for easy data analysis and sharing.
- **Error Handling**: Incorporates logging for error reporting and tracking feed parsing issues.
- **Default RSS Feeds**: Includes a set of default RSS feed URLs, with the ability to add more by editing a text file.

## Prerequisites
- Python 3.6 or higher.
- `feedparser` library installed (install via `pip install feedparser`).
- `pandas` library installed (install via `pip install pandas`).
- `openpyxl` library installed (install via `pip install openpyxl`), if you need to export to Excel format.

## Usage
1. **Run the Script**: Execute the `rss_aggregator.py` script in your Python environment.
2. **RSS Feed URLs**: Place your RSS feed URLs in a file named `feeds.txt`, one URL per line. If the file doesn't exist, the script will create it with default feeds.
3. **Check Console**: The script logs its progress and any errors encountered to the console.
4. **Review Output**: The script will store new articles in the database and print them to the console. It will also export the articles to `aggregated_articles.xlsx`.

## Security Considerations
Ensure that the RSS feed URLs are from trusted sources to prevent potential security risks associated with parsing content from unknown or untrusted websites.

## FAQs
Q: What is an RSS feed?
A: RSS (Really Simple Syndication) is a type of web feed that allows users and applications to access updates to online content in a standardized, computer-readable format.

Q: Why use a local database?
A: Storing articles in a database helps manage duplicates and provides a persistent storage mechanism that can be queried and analyzed.

Q: Can I export to formats other than Excel?
A: While the current script exports to Excel, `pandas` supports multiple formats. You can modify the `export_to_excel` function to export to CSV, JSON, or other formats supported by `pandas`.

## Troubleshooting
- **RSS Feed Parsing Errors**: Ensure that the RSS feed URLs are correct and that the feeds are properly formatted.
- **Database Issues**: Verify that the SQLite database file is not corrupted and that you have proper permissions to read/write to the database file.
- **Excel Export Problems**: Ensure that `openpyxl` is installed and that there are no issues with the Excel file path or permissions.

For further assistance or to report bugs, please open an issue on the project's issue tracker.
