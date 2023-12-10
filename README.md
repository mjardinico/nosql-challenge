## Title: Module 12 Challenge
### Submitted by: Michael Jardinico
### Date submitted: 12/10/2023

## Overview
`You have been hired by the editors of "Eat Safe, Love," a food magazine, to analyze food hygiene ratings data. These ratings are provided by the UK Food Standards Agency, which assesses a range of establishments throughout the United Kingdom for their food hygiene standards. Your analysis will guide the magazine's journalists and food critics in selecting locations for upcoming articles.`

`There are three parts to the data analysis for this project.`
- Part 1: Database and Jupyter Notebook setup:

1. Initial Setup: Use the NoSQL_setup_starter.ipynb notebook for this part of the challenge.

2. Import data from establishments.json using the Terminal. Name the database uk_food and the collection establishments. Copy the command used for importing data in a markdown cell within the notebook.

4. Import necessary libraries: PyMongo and Pretty Print (pprint).

5. Create an instance of the Mongo Client.

6. Confirm database creations: 
   - List all databases in MongoDB to confirm the presence of uk_food.
   - Check for establishments in the collections list of the uk_food database.
   - Use find_one and pprint to display a single document from the establishments collection.
