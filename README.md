# Beginner Friendly RSS Feed Aggregator

This script fetches articles from RSS feeds online, saves them to a database, and exports them to Excel. It's perfect for anyone wanting to easily aggregate articles from multiple websites into one place. 

## How It Works

The main steps are:

1. Loads list of RSS feed URLs from `feeds.txt` 
2. Uses Python's `feedparser` module to fetch articles from each feed
3. Stores article title, URL, publish date into a SQLite database 
4. Exports all saved articles to an Excel .xlsx spreadsheet

The script runs these steps automatically when executed. New articles are added every time it runs, while avoiding duplicate entries.

## Usage Guide

To use the script as a beginner:

### 1. Install Requirements

Python 3.x (latest version recommended)

Run `pip install feedparser pandas sqlite3` 

### 2. Save Feed List 

In the same folder as `aggregator.py`, create a `feeds.txt` file. 

On each line, add a single RSS feed URL to fetch articles from. For example:

```
https://www.npr.org/rss/rss.php?id=1001  
http://rss.cnn.com/rss/edition.rss
```

Save this file. Default feeds are added on first run if `feeds.txt` doesn't exist.

### 3. Run the Script

Open a terminal or command prompt and `cd` into the script folder. 

Run `python aggregator.py`

That's it! The script handles everything else automatically.

### 4. View Results

You'll now have:

- `aggregator.db`: SQLite database with fetched articles
- `aggregated_articles.xlsx`: Excel export of articles

New runs will append more articles to these outputs.

## Customization

See the script comments for areas you can customize like logging settings and the database schema.

## Let Me Know if You Have Any Other Questions!
