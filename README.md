# Mars Data Scraping and Analysis

## Introduction
This project involves scraping data from [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html) and [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html), and performing data analysis. The objective is to collect information about Mars news and Mars weather data, including temperature and atmospheric pressure. Additionally, the data analysis will provide insights into Mars climate patterns.

## Data Analysis

### Scrape Titles and Preview Text from Mars News
1. **Data Retrieval and Setup**
   - The script sets up the necessary libraries and establishes a connection to a specific Mars news website using Splinter and BeautifulSoup.

2. **Web Scraping**
   - It uses automated browsing to visit the Mars news site and inspects the page to identify the elements to be scraped.

3. **Data Extraction**
   - The code extract all the text elements from the identified elements on the website.

4. **Data Storage**
   - The extracted data is stored in a list of dictionaries, where each dictionary represents a title and its corresponding preview text.

### Scrape and Analyze Mars Weather Data
1. **Data Retrieval and Setup**
   - The script imports relevant libraries and establishes a connection to a Mars weather data website using Splinter and BeautifulSoup.

2. **Web Scraping**
   - Automated browsing is used to visit the Mars Temperature Data Site, and the page is inspected to identify the elements to be scraped.

3. **Data Extraction**
   - The code creates a Beautiful Soup object to parse the HTML content and extracts data from an HTML table.

4. **Data Storage**
   - The scraped data is assembled into a Pandas DataFrame with specific column headings. Unnecessary rows are removed and the DataFrame is reset.

5. **Data Preparation**
   - The data types of the DataFrame columns are examined and adjusted as needed for analysis.

6. **Data Analysis**

     ***Number of Months on Mars:***
    - To determine the number of months on Mars, the code groups the data by the 'month' column and then counts the unique values. This count represents the number of distinct Martian months included in the dataset.

     ***Total Data Count:***
    - The code counts the total number of data points in the dataset. This count reflects the cumulative data entries available for analysis, representing the duration of data collection.

     ***Coldest and Warmest Months:***
    - The code identifies the coldest and warmest months on Mars based on the minimum daily temperature (min_temp) recorded at the location of Curiosity, a Mars rover.
    - To find the coldest month, it calculates the average minimum temperature for each month and identifies the month with the lowest average.
    - To find the warmest month, it calculates the average minimum temperature for each month and identifies the month with the highest average.
    - Two separate bar charts are generated to visualize the coldest and warmest months, aiding in the interpretation of temperature patterns on Mars.

     ***Atmospheric Pressure Analysis:***
    - The code performs an analysis of atmospheric pressure at Curiosity's location on Mars.
    - It calculates the average daily atmospheric pressure for each Martian month.
    - The results are visualized in a bar chart, allowing for the easy identification of months with the lowest and highest atmospheric pressure.
    - This analysis provides insights into the variations in atmospheric pressure on Mars throughout the year.

     ***Mars Year Length Estimation:***
    - To estimate the length of a Martian year in Earth days, the code plots the daily minimum temperature data over time.
    - By observing temperature patterns and identifying peaks in the plot, an estimate of the Martian year's duration is made.
    - In the project's sample output, it is estimated that a Mars year is approximately 675 Earth days, and this estimate is visually confirmed using the temperature plot.


7. ***Data Export***
   - The resulting DataFrame is exported to a CSV file for future reference.


## Instructions
To run the project and access the data:

1. Ensure you have the required libraries and dependencies installed.
2. Run the Python script to perform the data scraping and analysis.
3. Review the 'output.csv' file for the gathered data and analysis results.
4. Feel free to adapt the code and URLs for further analysis or integration into other projects.