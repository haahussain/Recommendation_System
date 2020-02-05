# Employer Recommendation System
by Ali Hussain and Jay Kim

## Goal
To create a recommendation system that suggests the top potential employers based on the user's input of comparable employer(s). In other words, the user selects the preferred employer(s); then our system recommends other employers the user should consider based on similar features.

## Sources/Tools
Primary data gathered from Glassdoor.com:
* Considered the top 5,000 potential employers returned (using search results for New York City)


We created a content-based, item-to-item recommendation system using the K-Nearest Neighbors (Unsupervised Learning) algorithm along with:
* Beautiful Soup
* Selenium
* (MySQL Server)
* Scikitlearn library

## Exploratory Data Analysis
Bar graph Illustrating Popularity of Industry Type:
![EDAonIndustry](images/industry_count.png "count_for_industry")

Distribution of Overall Rating for all Companies: 

![EDAonOverallranking](images/overall_rating_distribution.png "distribution for overall rating")


#### Challenges
- Anonymous Users/Ratings: Cannot utilized collaborative filtering method approach
- Manual scraping (50 companies at a time)


## Features
Several Categories were too granular, and thus rolled up to broader categories:
* Industry: 84 rolled up to 12 categories
* Company Size: 8 rolled up to 4 categories
* Revenue: 14 rolled up to 4 categories

Sub-ratings were included as well with ratings from lowest to highest being 1-5:
* Culture & Values
* Work/Life Balance
* Senior Management
* Compensation and Benefits
* Career Opportunities

#### Modeling
- Nearest Neighbor Classification Model used to evaluate similarity across and between employers
- Various similarity metrics (Cosine, Minkowski, and Euclidean) were experimented with, along with 1-3 input companies
- (Preliminary test cases need to be further implemented)

#### Results
Lets say the following are our Top 3 favorite companies:
![Top3_companies_preferred](images/TOP3Again.png "Test Case our top3 companies")

The Top 5 most similar to our favorite companies using Cosine as distance metric would be: 
![New_Cosine_Metric](images/RESULTCOSINE.png "Test Case using Cosine Similarity Score")

The Top 5 most similar to our favorite companies using Minkowski as distance metric would be: 
![New_Minkowski_Metric](images/RESULTMINKOW.png "Test Case using Minkow Similarity Score")

###### The Winner
The Top 5 most similar to our favorite companies using Euclidean as distance metric would be: 
![New_Euclidean_Metric](images/RESULTEUC.png "Test Case using Euclidean Similarity Score")

#### Future Considerations
![InteractiveExample](scrapers/InteractiveVersion.jpg "Test Case Example using Interactive")
More Data!
* _Find & Merge Related Datasets (including broader set of features)_
* _Deeper Layers of both EDA and Modeling_
* _(if at all possible) Finding a way to include user-based data would open up many possibilities)_

#### Conclusions
* Euclidean similarity metric turned out to be the best metric because the top 5 recommended companies features were more relatable to our group of favorite companies. The results using the Euclidean metric were the most similar and comparable to our favorite 3 companies across the various features. 

