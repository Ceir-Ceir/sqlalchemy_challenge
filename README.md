# SQLAlchemy Challenge

## Setup

1. Create a new repository for this project called `sqlalchemy-challenge`. Do not add this assignment to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, create a directory for this Challenge. Use a folder name that corresponds to the Challenge, such as `SurfsUp`.
4. Add your Jupyter notebook and `app.py` to this folder. They’ll contain the main scripts to run for analysis. Also add the `Resources` folder, which contains the data files you will be using for this challenge.
5. Push the changes to GitHub or GitLab.

## Files

Download the following files to help you get started:

- [Module 10 Challenge files](#)

## Instructions

Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii. To help with your trip planning, you decide to do a climate analysis about the area. The following sections outline the steps that you need to take to accomplish this task.

### Part 1: Analyze and Explore the Climate Data

In this section, you’ll use Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database. Specifically, you’ll use SQLAlchemy ORM queries, Pandas, and Matplotlib. To do so, complete the following steps:

- Use the SQLAlchemy `create_engine()` function to connect to your SQLite database.
- Use the SQLAlchemy `automap_base()` function to reflect your tables into classes, and then save references to the classes named `station` and `measurement`.
- Link Python to the database by creating a SQLAlchemy session.

**Important**: Remember to close your session at the end of your notebook.

Perform a precipitation analysis and then a station analysis by completing the steps in the following two subsections.

#### Precipitation Analysis

1. Find the most recent date in the dataset.
2. Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
3. Select only the "date" and "prcp" values.
4. Load the query results into a Pandas DataFrame. Explicitly set the column names.
5. Sort the DataFrame values by "date".
6. Plot the results by using the DataFrame plot method.
7. Use Pandas to print the summary statistics for the precipitation data.

#### Station Analysis

1. Design a query to calculate the total number of stations in the dataset.
2. Design a query to find the most-active stations (that is, the stations that have the most rows).
3. List the stations and observation counts in descending order.
4. Answer the following question: which station id has the greatest number of observations?
5. Design a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.
6. Design a query to get the previous 12 months of temperature observation (TOBS) data.
7. Plot the results as a histogram with bins=12.

### Part 2: Design Your Climate App

Now that you’ve completed your initial analysis, you’ll design a Flask API based on the queries that you just developed. To do so, use Flask to create your routes as follows:

- `/`: Start at the homepage. List all the available routes.
- `/api/v1.0/precipitation`: Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value. Return the JSON representation of your dictionary. 

Let me know if you need further assistance! 😊
