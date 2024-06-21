# Freelancing-Shortlister

Project Overview
This project is designed to scrape job listings from Freelancer.com, filter them based on specific criteria, and store the filtered jobs in a database table. The main components of the project include web scraping, data filtering, and database interaction.

Features
Scrapes job listings from Freelancer.com
Filters jobs based on user-defined criteria
Stores filtered jobs in a database table
Requirements
Python 3.x
requests library
beautifulsoup4 library
pandas library
SQLAlchemy library
A database supported by SQLAlchemy (e.g., SQLite, PostgreSQL, MySQL)
Installation
Clone the repository:

bash

git clone https://github.com/yourusername/freelancer-job-scraper.git
cd freelancer-job-scraper
Install the required packages:

bash

pip install -r requirements.txt
Configure the database:

Modify the config.py file to set up your database connection. Example for SQLite:
python
Copy code
DATABASE_URI = 'sqlite:///jobs.db'
Usage
Run the scraper:

bash

python scraper.py
Filter the jobs:

You can define your filtering criteria in the filter_jobs function within scraper.py. Example:
python

def filter_jobs(jobs):
    return [job for job in jobs if job['budget'] > 100 and 'Python' in job['title']]
Store the jobs in the database:

The filtered jobs will be automatically stored in the database specified in config.py.
File Structure
scraper.py: Contains the main logic for scraping, filtering, and storing jobs.
config.py: Contains configuration settings for the project, including the database connection.
requirements.txt: Lists the dependencies required for the project.
README.md: Provides an overview and instructions for the project.
Contributing
Fork the repository.
Create a new branch: git checkout -b feature/your-feature-name.
Make your changes and commit them: git commit -m 'Add some feature'.
Push to the branch: git push origin feature/your-feature-name.
Submit a pull request.
