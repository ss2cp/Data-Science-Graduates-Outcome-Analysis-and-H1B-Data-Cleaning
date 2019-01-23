# Data Science Graduates Outcome Analysis and H1B Data Cleaning

This is an on-going personal enrichment project. I'm keeping a log-style readme for now to record my findings and ideas, until I delegate more time to work on this project full-time after application season.

## Jan. 18th 2019

Today, I was looking at different Data Science Programs and their graduates' career outcomes. Understandably, some programs either do not disclose post-graduate outcomes, or limit to high-level summary/percentage data. While it is to each individual program's liberty to disclose its data, post-graduate outcome is one of my main focuses when choosing MS Data Science programs, more generally, H1B visa sponsorship among international students. I have decided to look deeper into each program's websites to collect each student's career outcomes, which can be later compared with overall H1B Sponsorship data to see how hot data science really is. 

**I have concerns whether it is ethical/legal to collect students data. So far, all the data and datasets are public accessible. More research on such matter will be conducted as the project digs deeper.*

### Findings:

- Most programs list out all students in each class, due to small class sizes (50-75). Names of every student is also listed for most schools. 

- Full student name list for each class can be scraped with URLs, like ```.../stuents/2018```

- Some school websites show student's LinkedIn Page on student profiles.

- LinkedIn APIs do not allow public profile retrieval for developers. 

### Ideas:

- Get full lists of students in each program.

- Get LinkedIn profile URLs from website, if possible.

- Use Selenium to see each student's first full-time job after graduation on LinkedIn.

- Clean, summarize and visualize H1B datasets from the US Department of Labor.


### Files:

2016 H1B Data
2017 H1B Data
2018 H1B Data

## Jan. 22nd 2019

Today, I worked with Selenium to achieve automated login and search on qichacha.com, a Chinese enterprise-data website. The goal is to ge familiar with Selenium for later data scraping on LinkedIn. (and my boss asked me to do a research on partnership-companies of our Travel Management client) The process is very similar to searching in LinkedIn.

### Findings:

- URLs for each company profile are encoded by their own algorithms, like ```.../firm_52313235c549c109ff0c5ebbba7605d2.html```

- But search url remains constant with ```.../search?key=[CompanyName]```

- An inconvinience of converting Chinese into url can be solved with ```urllib.parse.quote([CompanyName])```

- Selenium uses a incognito-similar window in Chrome for operations. 

- Most websites do not allow too many search queries from the same IP address within certain timeframe. e.g. qichacha.com requires log in to paid membership after a certain threshold.

- This can be solved with a manual log in before automated process.

- At this point, most of my goals can be achieved, except for premium LinkedIn membership for unlimited search. 

### Ideas:

- I still remain concerns on the ethical part of this project. All the automated process done today is no different than hiring an intern to collect data.

## TO BE CONTINUED...
