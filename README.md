# Mission-to-Mars

## Overview
### Purpose
The purpose of this data analysis is to automate a web browser to visit different websites to extract data about the Mission to Mars. The data was then stored in a NoSQL database, and then rendered the data into a web application created with Flask. The completed work is then displayed in a portfolio.

The data analysis was done through 
- Gaining familiarity with and use HTML elements, as well as class and id attributes, to identify content for web scraping. 
- Using BeautifulSoup and Splinter to automate a web browser and perform a web scrape.
- Creating a MongoDB database to store data from the web scrape, a web application with Flask to display the data from the web scrape and an HTML/CSS portfolio to showcase projects.
- Using Bootstrap components to polish and customize the portfolio.

### Resources (Software)
- Python, Jupyter Notebook
- Pandas, BeautifulSoup, Splinter, ChromeDriverManager, Flask, PyMongo, 
- MongoDB, HTML5, Bootstrap 3

## Deliverable 1: Scrape Full-Resolution Mars Hemisphere Images and Titles
### Code is written that retrieves the full-resolution image and title for each hemisphere image
- Full code can be found in the [Mission_to_Mars_Challange](https://github.com/pfrivas/Mission-to-Mars/blob/main/Mission_to_Mars_Challenge.ipynb) file

### The full-resolution images of the hemispheres are added to the dictionary
```
img_url = hemispheres_soup.find('li').a.get('href')
```
### The titles for the hemisphere images are added to the dictionary
```
title = hemispheres_soup.find('h2', class_='title').text
```
### The list contains the dictionary of the full-resolution image URL string and title for each hemisphere image
```
hemispheres = {}
hemispheres['img_url'] = f'https://marshemispheres.com/{img_url}'
hemispheres['title'] = title
hemisphere_image_urls.append(hemispheres)
```
![img](https://github.com/pfrivas/Mission-to-Mars/blob/main/Resources/Hemisphere%20Dictionary%20List.png)
## Deliverable 2: Update the Web App with Mars’s Hemisphere Images and Titles
### The scraping.py file contains code that retrieves the full-resolution image URL and title for each hemisphere image
- The code can be found in the [scraping.py](https://github.com/pfrivas/Mission-to-Mars/blob/main/scraping.py) file
### The Mongo database is updated to contain the full-resolution image URL and title for each hemisphere image
- ![mongo_img](https://github.com/pfrivas/Mission-to-Mars/blob/main/Resources/MongoDB%20Code%20(Hemisphere%20Images).png)
### The index.html file contains code that will display the full-resolution image URL and title for each hemisphere image
- The code can be found in the [index.html](https://github.com/pfrivas/Mission-to-Mars/blob/main/templates/index.html) file
### After the scraping has been completed, the web app contains all the information from this module and the full-resolution images and titles for the four hemisphere images
![web_app_img1](https://github.com/pfrivas/Mission-to-Mars/blob/main/Resources/HTML%20Flask%20Web%20App.1.png)
![web_app_img2](https://github.com/pfrivas/Mission-to-Mars/blob/main/Resources/HTML%20Flask%20Web%20App.2.png)


## Deliverable 3: Add Bootstrap 3 Components
### The webpage is mobile-responsive
- ![mobile_img](https://github.com/pfrivas/Mission-to-Mars/blob/main/Resources/Flask%20Web%20App%20(Mobile).png)
### Two additional Bootstrap 3 components are used to style the webpage
- 1. 
- 2.
