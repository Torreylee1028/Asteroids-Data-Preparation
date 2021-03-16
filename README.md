# Asteroids

## Data Preparation

### Introduction

This project consisted of cleaning data from three different sources: a flat file, scraping a website, and connecting to an API. the cleaning of the data utilizes pandas DataFrame. The final product included joining all three sources on the same key by storing them in a SQLite database. 

The final database contained information on asteroids, how much they would be worth if we were to mine them, and if they are a near earth object. The most challenging piece was creating a common key to join the data frames on. Each source used a slightly different nomenclature for naming the asteroids, which needed to be uniform to join them on the same key.

### Tools:
* Pandas
* BeautifulSoup
* Sqlite3

### Part 1 – Flat File Source

The first part of this project was to load a flat file such as a CSV and clean the data.

Source: JPL Small-Body Database Search Engine: https://ssd.jpl.nasa.gov/sbdb_query.cgi#x

* Demonstrated the following data preparation techniques:
  * Rename columns
  * Strip whitespace in front of asteroid names
  * Change a column type to Boolean
  * Fill in missing values
  * Change measurement of a column from kilometer to miles

### Part 2 – Website Source

The second part of the project was to use BeautifulSoup and scrape a website to retrieve data.

Source: Asterank: https://www.asterank.com/

*	Demonstrated the following data preparation techniques:
    * Rename columns
    * Utilize regular expressions to remove three characters that the scraped data pulled that shouldn’t be there
    * Map a long description to the shortened code respectively
    * Change column from reflecting a string of “100 million” to numeric representation “100,000,000”
    * Bin columns based on values

### Part 3 – API Source
The last data source came from connecting to an API to pull the data.

Source: NASA APIs: https://api.nasa.gov/

*	Demonstrated the following data preparation techniques:
    * Unpack a column that contained a dictionary into multiple columns
    * Rename columns 
    * Drop columns
    * Change a date column from an object type to datetime type to utilize datetime features 

### Part 4 – Asteroid Database
*	Demonstrated the following:
    * Creating a SQLite database 
    * Creating three separate tables
    * Performing both an outer join and an inner join to combine all three tables
