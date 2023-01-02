# 12_News_Weather

## Part 1 = Mars News

### Prep - Part 1

Using the provided code, I imported the dependencies and set up the exectuable path and browser.

### Step 1: Visiting and Inspecting the Website

I Set up the NASA Mars Science as my URL and browsed and inspected the site.

### Step 2: Using Beautiful Soup to Extract the text

I created a Beautiful Soup Object and Extracted all the text results with the code:

`results = soup_response.body.find_all('div',class_='list_text')`

### Step 3: Storing the Results

1. Made an empty list for the dictionaries
2. Looped through the text elements 
3. Extracted the title and preview text from the elements
4. Stored each title and preview pair in a dictionary
5. Added the dictionary to the list
6. Printed the list
7. Quit the Browser

## Part 2: Mars Weather Analysis

### Prep - Part 2

Using the provided code, I imported the dependencies and set up the exectuable path and browser.

### Step 1: Visiting and Inspecting the Temperature Website

Set up the Mars Temperature Data Site as my URL and browsed and inspected the site.

### Step 2: Scraping the Temperature table

1. Created a Beautiful Soup Object
2. Extracted the table data with this code, and printed it prettified.
`results = soup_response.table.find_all('tr', class_="data-row")`

### Step 3: Store the Data in a Pandas DataFrame

1. Created a Pandas DataFrame by using the list of the column names.
2. Looped through the table rows to find the data for each column - text only. 
3. Appended the Dataframe with all the column data.
4. Printed the Dataframe to make sure it was there.

### Step 4: Prepare the Data for Analysis

1. Examined the data in each column to look for data types.
2. Removded "ls" columns that were empty (had 0 as entry and then was stripped in constructing the dataframe).
3. Changed the data types for each column.
4. Confirmed the new data types.

### Step 5: Analyse the Data

1. Used Pandas `.max()` function to determine the number of months on Mars and printed using text fomatting.
2. Used the `.max() and .min()` functions to find the number of days of data and printed.
3. Used the `.groupby('month').agg('min_temp':'mean')` to determine and display the average minimum temperature by month on Mars.
4. Made this into a separate dataframe and plotted the avg min_temp using `.plot()` function.
5. Used the `groupby("month").agg({"ls":"mean", "min_temp":"mean"})` to determine and display the avg min-temp by month based on the averge location of the Curiosity Rover.
6. Used the `.groupby("month").agg({"pressure":"mean"})` to determine the average pressure by month.
7. Created a separate dataFrame for it and plotted the avg pressure data.
8. Plotted the 'min_temp' by "sol", examined the sols between peaks and estimated 700 days per martian year.

### Step 6: Saved the DataFrame to a CSV file.

1. Saved the dataframe to a .csv file
2. Quit the Browser





