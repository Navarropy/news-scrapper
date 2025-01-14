# Headline Extractor and Organiser

This Python script extracts news headlines from CNN and Fox News, stores them in a SQLite database, and exports them to an Excel spreadsheet with formatting.

## Features

* **Extracts headlines from multiple websites.** [1]
* **Filters out empty or short headlines.** [2]
* **Stores headlines and their source in a SQLite database.** [3, 4]
* **Exports data to an Excel spreadsheet.** [4]
* **Applies formatting to the spreadsheet for better readability.** [5]

## Requirements

* Python 3
* Libraries: `requests`, `lxml`, `sqlite3`, `pandas`, `openpyxl`

## Usage

1. Install the required libraries.
2. Run the script. 
   * This will create a database named `headlines.db` and an Excel spreadsheet named `headlines.xlsx`. 

## Output

* `headlines.db`: A SQLite database containing a table with the following columns:
    * `id`: Auto-incrementing primary key
    * `headline`: The extracted headline
    * `website`: The source website (e.g., CNN, Fox News)
* `headlines.xlsx`: An Excel spreadsheet containing the same data as the database, with the following formatting:
    * **Bold and centred headers**
    * **Adjusted column widths for readability**

![image](https://github.com/user-attachments/assets/0fa6fbc0-2c0f-4447-b1ae-17a82dd9245d)

## Note

The script uses XPath to extract headlines from the target websites. If the websites change their structure, the XPath expressions may need to be updated. [1, 2]
