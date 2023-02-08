# Obama's Favourite Movies Analysis
:movie_camera: A visual dashboard of Barack Obama's Favourite Movies since 2018 :movie_camera:

## Overview (TL;DR)

This project is a data scraping and visualizaton exercise on Obama's annual year-end movie list. 

- Data Source:  
  - List of movie names was scraped from https://www.yearendlists.com/
  - Corresponding movie information was scraped from Rotten Tomatoes or Wikipedia (the latter was used if not available on RT) using Beautiful Soup
  
- Visualization: 
  - Conducted using Plotly, visible on html file attached *Note: Current file attached is the working file*

- Jupyer notebook/code: *Note: To be uploaded*

## Data Scraping

Data or Web Scraping is a technique for obtaining and importing data from a website into a local file. It essentially allows individuals to 'copy and paste' but on an automated level and at a greater capacity.

## Data Extraction and Cleaning 

There are 3 major steps to data scraping:
1. Request data - Using HTTP link
2. Get data - Extract and parse 
3. Save data - To local file 

There are many tools that can be used to scrape data. Python has many open-source libraries that facilitate web scraping, including Beautiful Soup (which I used for my project), Scrapy, and Selneium. There are a few online tools that are available, including but not limited to ParseHub, import.io, and Scrape.do. Microsoft Excel also offers data scraping capabilities using dynamic web queries. 

Note that many websites offer APIs to easily access data (in this case, Rotten Tomatoes and Wikipedia have this option). However, I chose to use Beautiful Soup to scrape all of the final data in my dataset.

As Obama typically publishes his list of movies on an image file, I first obtained a list from a website where these were all tabulated. I then used Rotten Tomatoes to to scrape the key movie information I wanted to extract, including genre, budget, the audience and critic sources rotten vs fresh status, etc. As all movie urls did not necesarily follow the same format- specifically if another movie already exists with the same name- this happened over a few steps until I successfully extracted any information for each movie on its respective RT page. Due to the small number of movies on the list (just over 80), if any key features I wanted to use in my analyze was not available on Rotten Tomatoes, I then filled in the missing information from Wikipedia.

Once all data was compiled, additional cleaning was done to separate movie information with multiple values into separate columns (i.e. if multiple producers, genres, etc. are listed). 

## Final Visualization and Findings

The final data was graphed and visualized using plotly. *Final file to be uploaded*


## Disclaimer

Please note that the data obtained from this project is for an amateur proejct and was not to be used for any financial or personal gain. 

