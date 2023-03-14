# Obama's Favourite Movies Analysis
:movie_camera: A visual dashboard of Barack Obama's Favourite Movies since 2018 :movie_camera:

## Overview (TL;DR)

This project is a data scraping and visualization exercise on Obama's annual year-end movie list. 

- Data Source:  
  - List of movie names was scraped from https://www.yearendlists.com/
  - Corresponding movie information was scraped from Rotten Tomatoes or Wikipedia (the latter was used if not available on RT) using Beautiful Soup
  
- Jupyer notebook/code: Done in Python, separated into 2 notebooks:
i) Obama Favourites List - Web Scraping.ipynb 
ii) Obama Favourites List - Plotly.ipynb

- Visualization: 
  - Graphs were created using Plotly, with interactive dashboard visualization using Dash  


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


## Data Visualization

All graphs were visualized using Plotly and deployed on an interactive dashboard application using Dash. Dash is an open-source framework for building data visualization interfaces written on top of Plotly and React. 
Dash apps are made interactive through Dash Callbacks, which for my mine is based on the selected year. The responsive app design and layout was built using Dash bootstrap components (documentation is available here: https://dash-bootstrap-components.opensource.faculty.ai/docs/).

## Final Visualization

Here is a walkthrough of my app:

![Obama Dashboard](https://user-images.githubusercontent.com/104465263/219374690-3f5b1545-e394-4a73-b8f8-860cfe307e61.gif)



## Disclaimer

Please note that the data obtained from this project is for an amateur project and is not to be used for any financial or personal gain. 

