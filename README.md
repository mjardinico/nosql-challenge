## Title: Module 12 (NoSQL Challenge)
`Submitted by: Michael Jardinico`
`Date submitted: 12/10/2023`

## Overview
`You have been hired by the editors of "Eat Safe, Love," a food magazine, to analyze food hygiene ratings data. These ratings are provided by the UK Food Standards Agency, which assesses a range of establishments throughout the United Kingdom for their food hygiene standards. Your analysis will guide the magazine's journalists and food critics in selecting locations for upcoming articles.`


`There are three parts to the data analysis for this project.`
### Part 1: Database and Jupyter Notebook setup:
1. Initial Setup: Use the NoSQL_setup_starter.ipynb notebook for this part of the challenge.
2. Import data from establishments.json using the Terminal. Name the database uk_food and the collection establishments. Copy the command used for importing data in a markdown cell within the notebook.
4. Import necessary libraries: PyMongo and Pretty Print (pprint).
5. Create an instance of the Mongo Client.
6. Confirm database creations: 
   - List all databases in MongoDB to confirm the presence of uk_food.
   - Check for establishments in the collections list of the uk_food database.
   - Use find_one and pprint to display a single document from the establishments collection.

### Part 2: Update the Database
`The magazine editors have requested modifications for the database before performing any queries or analysis for them. Make the following changes to the establishments collection`
1. Use `NoSQL_setup_starter.ipynb` for this section of the challenge
2. Include the new halal restaurant to the establishments collection with details as follows:
    `{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
    }` 

3. Update the `BusinessTypeID` and `BusinessType fields`
4. Delete all entries with `LocalAuthorityName` called `Dover` 
5. Convert `latitude` and `longitude` to decimal numbers while `RatingValue` as Integer

### Part 3: Exploratory Analysis
#### Question 1: Which establishments have a hygience score equal to 20?
    - Perform a query to find establishments with hygience score of 20
    - Use `count_documents()` for correct number of documents
    - Convert to Pandas DataFrame and displays the first 10 rows

#### Question 2: Which establishments in London have a `RatingValue` greater than or equal to 4?
    - Perform a query to find the establishments with RatingValue greater than or equal to 4
    - Use $regex operator to locate the London establishments
    - Use pprint for the first result
    - Convert to Pandas DataFrame and display the first 10 rows
 
#### Question 3: What are the top 5 establishments with `RatingValue` of 5?
    - Perform a query to find the establishments with `RatingValue` of 5
    - Use the `sort()` method to sort in ascending order on the hygiene score
    - Use the `limit()` method to limit the results to 5. Use pprint to display results.
    - Convert the result to Pandas DataFrame

#### Question 4: How many establishments in each Local Authority have hygiene score of 0?
    - Create a pipeline and match establishments with hygience score or 0
    - Group the matches by Local Authority (LocalAuthorityName)
    - Sort the matches from highest to lowest
    - Print the first 10 results
    - Convert the results to Pandas DataFrame

