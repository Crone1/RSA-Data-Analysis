# Overview
This repository contains all of the code written to process data from the Irish Road Safety Authority (RSA) from 2005 to 2012 as part of the college module *'Data Processing and Visualisation'*.

The goal of this project was to clean the road safety data, get it into a nice format and then to perform visual analysis on the processed data.



# Process Description

List of tools used:

    Jupyter Notebook
    OpenRefine
    

Review of processing stage:

    I started this project with the idea that I would go through and process each of the 5 different datasets one at a time seperatly.
    I processed the first 3 datasets into their own dataframes taking note of the previous excercise we had done in class on reading data into a dataframe in pandas.
    I skipped the 2010 second excel dataset as I figured that this would be more difficult than the other ones.
    I processed the last 2 datasets into their own dataframes and when it was time to come back to this dataset, I didnt know of any way to restructure this data within Jupyter notebook, so I decided to make a copy of this file and then restructure it in excel.
    This choice saved me a good bit of hassle and this dataset was then no harder to work with than the other datasets.
    I was also able to spot and clean an error within the data in excel as a result.
    I made sure all of the dataframes were layed out the same for when it came time to join them together.
    Overall, the steps that I had to take to sort all of the different datasets into a uniform layout were pretty similar for each dataset.
    There were some minor differences but once I got the hang of what to do for the first few, I had a very good idea how to approach the other datasets, bar the 2010 one which I had to use an external programme to aid the processing phase of this dataset.
    Once all of these datasets were processed, it was just a matter of joining them together and then cleaning the data.
    I wanted to order this final dataframe by Year, Age, Sex, Participant, Casualty, Total in that order which I did have a bit of trouble with; however, I got this sorted in the end after a bit of googling and reworking.

Link to the Processed dataframe as a CSV:

    http://localhost:8888/edit/2019-ca273-cronen2-a1/data/processed/Processed_dataframe-csv.csv

Link to file describing how I cleaned the dataframe:

    http://localhost:8888/edit/2019-ca273-cronen2-a1/notebooks/Cleaning.md
    
Link to the notebook that I used to help clean the dataframe:

    http://localhost:8888/notebooks/2019-ca273-cronen2-a1/notebooks/Analysing%20the%20cleaned%20dataframe.ipynb
    
    
Review of the cleaning stage:

    For the cLeaning, I knew I was going to use OpenRefine so I knew I would have to export the dataframe from the notebook to a CSV to open it in OpenRefine.
    Once I had this file opened in OpenRefine, it was pretty easy to clean the data with this application.
    There were not many errors so these were easy enough to spot especially with how easy OpenRefine is to use with its 'Text Facet' button.
    In OpenRefine I did notice an odly large value of '1010' in the 'Total' column which I did want to investigate further as I didn't have enough information at that time to change the value.
    To investigate this, I wanted to transfer this csv back into Jupyter Notebook to compare this value with the other totals, and the totals of rows with these same attributes in other years.
    After doing this, I decided to change this value.
    After this cleaning, I just had to export this cleaned table and then that was the practical side of the project done.

A CSV of the data after it had been cleaned in OpenRefine can be found at 'data/processed/Cleaned_dataframe-csv.csv'.

A bit of extra work I did on notebooks:

    Near the end of the processing stage and of writing the notbook, I decided that my current notebook of my processing stage was quite long and a bit messy so I decided to write a Summary notebook of this stage.
    I wanted to have a notebook that was more compact and to the point for Suzanne so that it was easier for her to look through.

The final CSV of the cleaned and processed data can be found at 'data/processed/Final_dataframe-csv.csv'.
