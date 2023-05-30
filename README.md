# WikiScrape

This repository contains two scripts: `WikiScrape.ipynb` and `getTitles.ipynb`.

### WikiScrape.ipynb

The `scrape_wikipedia.py` script is designed to scrape content from Wikipedia articles using the Wikipedia-API library in Python. It retrieves article titles from a CSV file, checks for progress using a JSON file, and saves the scraped content as text files. The script also includes a post-processing step to remove specific files from the scraped directory based on specified criteria.

#### Installation

To use this script, you need to install the `Wikipedia-API` library. You can do this by running the following command:

```
! pip install Wikipedia-API
```

#### Usage

1. Set the appropriate paths for the database (DB) and progress storage.
2. Import the necessary libraries: `wikipediaapi`, `re`, `pandas`, `tqdm`, `json`, and `os`.
3. Define the `clean_text` function to remove unwanted elements from the scraped text.
4. Create an instance of the Wikipedia-API client.
5. Define the `scrape_wikipedia_article` function to retrieve the content of a Wikipedia article.
6. Iterate over the article titles and scrape the content for each title, skipping already scraped articles.
7. Save the scraped content as text files and update the progress file.
8. Perform post-processing on the scraped files by specifying strings to search for in the filenames and removing matching files.
9. Display the number of remaining files in the database directory.

Note: Make sure to modify the file paths and customize the script according to your needs.

### getTitles.ipynb

The `getTitles.ipynb` notebook provides a way to extract article titles from an XML dump of a Wikipedia database. It uses the `xml.etree.ElementTree` and `csv` libraries in Python to open and parse the XML file, retrieve the titles of the pages, and save them into a CSV file.

#### Usage

1. Obtain the XML dump of the desired Wikipedia database from [https://dumps.wikimedia.org/](https://dumps.wikimedia.org/) by selecting the appropriate language identifier and the latest available dump.
2. Open the `getTitles.ipynb` notebook.
3. Import the necessary libraries: `xml.etree.ElementTree` and `csv`.
4. Specify the path to the XML dump file.
5. Parse the XML file and define the XML namespace.
6. Retrieve the titles of the pages and store them in a list.
7. Save the titles into a CSV file named `titles.csv`.
8. The generated `titles.csv` file may require post-processing to remove irrelevant information.

### License

These scripts are released under the [MIT License](https://opensource.org/licenses/MIT).
