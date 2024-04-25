# data-sourcing-challenge
Module 6 Challenge

## Background
You've been tasked to prepare some data for a recommendation system to help people find movie reviews and related movies. You will extract data from two different sources: The New York Times API and The Movie Database, then merge the data together. The text extracted from these APIs can later be used with natural language processing methods.

## Before you begin
- Before starting the assignment, be sure to complete the following steps:
   - [x] Create a new repository for this project called data-sourcing-challenge. **Do not add this homework assignment to an existing repository.**
   - [x] Clone the new repository to your computer.
   - [x] Inside your local Git repository, add the starter files retrieve_movie_data.ipynb and example.env from your file downloads
   - [x] Rename example.env to .env and add your API keys to the file.
   - [x] Ensure the .env file is not listed when you perform a git status check on the repo, before performing your git add action.
   - [x] Push these changes to GitHub or GitLab.

> [!NOTE]
> The CSV file included in the output folder in your starter files is to help you identify how your final CSV file should be structured. Do not copy this file to your own repo. You will instead upload the CSV file you create as part of the Challenge.


## Instructions
This Challenge has three parts, and must be completed in order:

- Part 1: Access the New York Times API.

- Part 2: Access The Movie Database API.

- Part 3: Merge and Clean the Data for Export.

The starter code includes importing the required dependencies and your API keys from your .env file, but you will need to ensure your API keys are added to that file.

## Part 1: Access the New York Times API
1.  The base URL is included in the starter code, along with the search string and query dates. Consult the New York Times Article Search API documentationLinks to an external site. to help you build your query_url using these variables.

If you accidentally delete these variables, they are:

![image](files:/C:/Users/porti/OneDrive/Pictures/Screenshots/Challenge_6_image1.png)


2.  Check that the columns in the two DataFrames have similar names and data types.

3. Combine the two DataFrames by the rows using an inner join, and reset the index.

> [!TIP]
> **Read over the instructions to determine if you should use concat, join, or merge.**

4. After combining the DataFrames, do the following:

    - Check if there are any null values.

    - Check each column’s data type.

    - Convert the "invoice_date" column to a datetime data type.


## Determine which Region Sold the Most Products
1. Use either the groupby or pivot_table function to create a multi-index DataFrame with the "region", "state", and "city" columns.

2. Rename the aggregated column to reflect the aggregation of the data in the column.

3. Sort the results in descending order to show the top five regions, including the state and city that have the greatest number of products sold. Your final table should look like the following image:


## Determine which Region had the Most Sales
1. Use either the groupby or pivot_table function to create a multi-index DataFrame with the "region", "state", and "city" columns.

2. Rename the aggregated column to reflect the aggregation of the data in the column.

3. Sort the results in descending order to show the top five regions, including the state and city that generated the most sales. Your final table should look like the following image:

## Determine which Retailer had the Most Sales
1. Use either the groupby or pivot_table function to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.

2. Rename the aggregated column to reflect the aggregation of the data in the column.

3. Sort the results in descending order to show the top five retailers along with their region, state, and city that generated the most sales. Your final table should look like the following image:

## Determine which Retailer Sold the Most Women's Athletic Footwear
1. Filter the combined DataFrame to create a DataFrame with only women's athletic footwear sales data.

> [!TIP]
> **Use df[df["column_name"].str.contains("<value>")] or df.loc[(df["column_name"] =="<value>")].**

2. Use either the groupby or pivot_table function to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.

3. Rename the aggregated column to reflect the aggregation of the data in the column.

4. Sort the results in descending order to show the top five retailers along with their region, state, and city that sold the most women's athletic footwear. Your final table should look like the following image:

## Determine the Day with the Most Women's Athletic Footwear Sales
1. Create a pivot table with the "invoice_date" column as the index and the "total_sales" column as the values parameter.

2. Rename the aggregated column to reflect the aggregation of the data in the column.

3. Apply the resample function to the pivot table, place the data into daily bins, and get the total sales for each day.

4. Sort the resampled DataFrame in descending order to show the top 10 days that generated the most women's athletic footwear sales. Your final table should look like the following image:

## Determine the Week with the Most Women's Athletic Footwear Sales
1. Apply resample to the pivot table above, place the data into weekly bins, and get the total sales for each week.

2. Sort the resampled DataFrame in descending order to show the top 10 weeks that generated the most women's athletic footwear sales. Your final table should look like the following image:

## Hints and Considerations
- Consider what you've learned so far. You’ve learned how to combine data using concatenation, joins, and merging, and how to reshape data using groupby, pivot, pivot_table, resample, and melt functions.

- If you're struggling with how to start, look back on some of the activities you did in class.

- Always commit your work and back it up with pushes to GitHub or GitLab. You don't want to lose hours of your hard work! Also make sure that your repo has a detailed README.md file.

## Badges

## Visuals

## Installation

## Usage
This assigment highlights the usage of groupby and pivot table functions for analyzing sales information for athletic apparel sales in the United States.

## Support
Some of the code on this assigment was done with the help of a bootcamp tutor.

## Roadmap

## Contributing

## Authors and acknowledgment
1. Code generated with the assistance of Vijaya (@Bootcamp Tutor)
2. Reference material - [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)
3. Python HOWTOs - [https://docs.python.org/3/howto](https://docs.python.org/3/howto/index.html)
4. This site was built using [GitHub Pages](https://pages.github.com/).

## License


## Project status
- Submitted for grading (04.18.2024)

## Footnotes
Sales Product Data. Available: (https://www.kaggle.com/datasets/knightbearr/sales-product-dataLinks) to an external site.
