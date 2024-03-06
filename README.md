# Gold Medal Metrics – Olympic Data Reporting Web Application

### Overview


This comprehensive project integrates Java with Spring Boot and SQL for backend functionality, while incorporating JavaScript, CSS, and HTML for frontend UI/UX development. This project is designed to manage and present gold medal data for various countries. It includes models to represent data objects, interface repositories to interact with these models, and an SQL database to store the objects. Additionally, this project's Spring Boot application is responsible for handling HTTP requests related to gold medal data for countries - it provides endpoints to fetch lists of countries, detailed country information, and country-specific gold medal data. The project interacts with repositories for country, gold medal data and its attributes, processes requests for sorting and filtering, and generates appropriate JSON responses for clients.

![image](https://github.com/DeafinitelyAbled/Gold_Medal_Metrics_Project/assets/135254827/1169e800-a9ee-42a1-a192-1ccba633b292)

# Instructions
### - Downloading Instruction:
1) Download and open a ZIP File.
2) Copy / paste the file locally and run it on your preferred IDE. 
3) Run the main code (src -> java -> GoldMedalApplication.java).
4) Open *http://localhost:3001/* on the web browser.
5) Check out the list of data and its attributes.
6) Click on traingle shaped icons to sort the attributes ascendingly / descendingly.
7) Search for a country of your preference and enjoy exploring the data!

### - Testing Instruction:

You can use cURL statement in Command Prompt / Terminal to manually test the API endpoints. 

Here are some example cURL requests and responses:

- Get countries, sorted by its name in ascending order 

```shell
curl "http://localhost:3001/countries?sort_by=name&ascending=y"                                   

{"countries":[{"name":"Afghanistan","code":"AFG","gdp":594.32,"population":32526562,"medals":0},...]}
```

- Get the details for the United States Olympic team

```shell
curl "http://localhost:3001/countries/united%20states"                                            

{"name":"United States","gdp":"56115.72","population":"321418820","numberMedals":"2477","numberSummerWins":"2302","percentageTotalSummerWins":"21.957268","yearFirstSummerWin":"1896","numberWinterWins":"175","percentageTotalWinterWins":"9.1098385","yearFirstWinterWin":"1924","numberEventsWonByFemaleAthletes":"747","numberEventsWonByMaleAthletes":"1730"}

```

- Get the list of Gold medal winners for the United States Olympic team, sorted by the athlete's name in descending order

```shell
curl "http://localhost:3001/countries/united%20states/medals?sort_by=name&ascending=n"            

{"medals":[{"year":1968,"city":"Mexico","season":"Summer","name":"ZORN, Zachary","country":"United States","gender":"Men","sport":"Aquatics","discipline":"Swimming","event":"4X100M Freestyle Relay"},...]}
```

