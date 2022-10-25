# RottenTomatoes Scraper

* Selenium to create a Python Notebook with a python function called scrape(driver, url) <br>
* The function should accept 2 parameters: <br>
* driver: the selenium webdriver (bridge) that connects python to chrome. This is exactly the same parameter that we used in class. <br>
* url: the link to the reviews page for a specific movie on rottentomatoes (e.g. https://www.rottentomatoes.com/m/exodus_gods_and_kings/reviewsLinks to an external site.<br>
* The function should then scrape all the reviews across all review pages that are available for the movie. <br>
* The function should create a csv file called 'output.csv' that includes 1 row for each review and the following fields for each row: <br>
* reviewer's name, review date, review text, review_polarity <br>
* All fields should appear in the csv exactly as they appear on the website <br>
* review_polarity should be 'rotten' or 'fresh', depending on the green/red icon attached to the review. <br>

