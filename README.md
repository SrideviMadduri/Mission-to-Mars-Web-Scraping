# Mission-to-Mars-Web_Scraping

In this project, full web-scraping and data analysis for the mission to Mars is done. In this project we used Beautiful Soup for HTML parsing, automated browsing with Splinter, Matplotlib and pandas to extract data  related to Mission to Mars.

This project consists of two parts :

Part 1: Scrape titles and preview text from Mars news articles. Exporting the data into a JSON file and a MongoDB database.

Part 2: Scrape and analyze Mars weather data, which exists in a table.

## Part 1: Scrape Titles and Preview text From Mars News

- Created a Jupyter Notebook named part_1_mars_news.ipynb.
- Used automated browsing to visit the link https://redplanetscience.com/ . Inspected the page to identify which elements to scrape by inspecting the page using Chrome     DevTools.
- Created a Beautiful Soup object and used it to extract text elements from the website.
- Extracted the titles and preview text of the news articles that we scraped. Store the scraping results in Python data structures as follows:
  - Stored each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: title and preview.
  - Stored all the dictionaries in a Python list.
  - Printed the list in your notebook.
- Stored the scraped data in a file and to  database (to ease sharing the data with others). To do so, exported the scraped data to  a JSON file and a MongoDB database.

## Part 2: Scrape and Analyze Mars Weather Data

- Created a Jupyter Notebook named part_2_mars_weather.ipynb.
- Used automated browsing to visit the Mars Temperature Data https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html. Inspected the page to identify which     elements to scrape by inspecting the page by using Chrome DevTools to discover whether the table contains usable classes.
- Created a Beautiful Soup object and used it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function.           However, used Beautiful Soup here to continue sharpening web scraping skills.
- Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column           headings:

  - id: the identification number of a single transmission from the Curiosity rover
  - terrestrial_date: the date on Earth
  - sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
  - ls: the solar longitude
  - month: the Martian month
  - min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
  - pressure: The atmospheric pressure at Curiosity's location
- Examined the data types that are currently associated with each column. Used the Pandas astype and to_datetime cast (or convert) the data to the appropriate           datetime, int, or float data types.
- Analyzed the dataset by using Pandas functions to answer the following questions:
  1. How many months exist on Mars?
  2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
  3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
     - Found the average the minimum daily temperature for all of the months.
     - Ploted the results as a bar chart.
  4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    - Found the average the daily atmospheric pressure of all the months.
    - Ploted the results as a bar chart.
  5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
     - Considered how many days elapse on Earth in the time that Mars circles the Sun once.
     - Visually estimated the result by plotting the daily minimum temperature.
  6. Exported the DataFrame to a CSV file.
















