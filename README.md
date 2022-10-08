# Human Centered Data Science -Homework_1

This repository contains the necessary material (data and code) with analytical results (plots) to reproduce the similar results to understand the time series data for the number of articles on dinosaurs visited by users using mobile (from web and app) and desktop on wikipedia from July 2015 through October 2022 . This analysis was done as the part of my homework for Human Centered Data Science at The University of Washington- Seattle. 

The goal of the assignment was to collect the data using API, clean the data and generate analytical results keeping reproducibility in mind.All the necessary details about the data and code has been explicitly given to make sure that if the other person looks at this repository, it should be easy to reproduce the same results. 

## API Documentation

The data for this analysis was used from the Page View API [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts)

The data curated from this API gives the monthly granularity for the number of users visiting dinosaur articles on wikipedia. 

## Directory Structure
The directory structure for the repository is shown below

```

.
├── raw_files
│   ├── dino_monthly_desktop_start201501-end202209.json
│   ├── dino_monthly_mobile-app_start201501-end202209.json
│   ├── dino_monthly_mobile-web_start201501-end202209.json
│   ├── dino_monthly_mobile_start201501-end202209.json
│   ├── dinosaur_genera_cleaned.csv
├── json_output
│   ├── dino_monthly_desktop_start201501-end202209.json
│   └── dino_monthly_mobile_start201501-end202209.json
│   └── dino_monthly_cumulative_start201501-end202209.json
├── plots
│   ├── Max_Average_and_Min_Average_Page_Requests_for_Desktop_and_Mobile.png
│   ├── Top_10_Articles_by_Peak_Page_Views_and_Access_Type.png
│   └── Bottom_10_Articles_with_Fewest_Months_of_Data_for_Desktop_and_Mobile_Each.png
├── src
│   └── hcds-a1-data-curation.ipynb
├── README.md
└── LICENSE
```

## Data Description
The columns in each of the json file are the same and the description of the same has been mentioned below:

**JSON FILE**
This file contains the information at monthly granularity about the dinosaur articles and has been generated using the API mentioned above under API Documentation
---------------------------------------------------------------------------------
| Column                    | Description                                                           |
| ------------------------- | ----------------------------------------------------------------------|
| `year`                    | The year of the data point                                            |
| `month`                   | The month of the data point.                                          |
| `date`                    | The year-month pair serve as a key                                    |
| `log_views`               | The natural log of the views column                                   |
| `access`                  | Data contains three different access: desktop, mobile-app, mobile-web |
| `article`                 | This is the name of the articles we are pulling on Wikipedia          |
-----------------------------------------------------------------------------------------------------

**CSV FILE**
This file contains the dinosaur names and the respective urls for the wikipedia pages.
---------------------------------------------------------------------------------
| Column                    | Description                                                           |
| ------------------------- | ----------------------------------------------------------------------|
| `name`                    | name of the dinosaur                                                  |
| 'url'                     | url for the article for the dinosaur under name column                |                
-----------------------------------------------------------------------------------------------------

## Visualization

![Maximum Average and Minimum Average](Max_Average_and_Min_Average_Page_Requests_for_Desktop_and_Mobile.png)

![Top 10 Peak Page Views](Top_10_Articles_by_Peak_Page_Views_and_Access_Type.png)

![Bottom 10 Articles](Bottom_10_Articles_with_Fewest_Months_of_Data_for_Desktop_and_Mobile_Each.png)

## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)

