# RottenTomatoes Scraper

Use selenium to create a Python Notebook with a python function called scrape(driver, url)
The function should accept 2 parameters:
driver: the selenium webdriver (bridge) that connects python to chrome. This is exactly the same parameter that we used in class. 
url: the link to the reviews page for a specific movie on rottentomatoes (e.g. https://www.rottentomatoes.com/m/exodus_gods_and_kings/reviewsLinks to an external site.
The function should then scrape all the reviews across all review pages that are available for the movie. 
The function should create a csv file called 'output.csv' that includes 1 row for each review and the following fields for each row:
reviewer's name, review date, review text, review_polarity
All fields should appear in the csv exactly as they appear on the website
review_polarity should be 'rotten' or 'fresh', depending on the green/red icon attached to the review.

