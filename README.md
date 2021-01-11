# Overview
This repository contains all of the code written to process data from the Irish Road Safety Authority (RSA) from 2005 to 2012 as part of the college module *'Data Processing and Visualisation'*.

The goal of this project was to clean the road safety data, get it into a nice format and then to perform visual analysis on the processed and cleaned data.
This was done using Jupyter Notebooks, OpenRefine and Plotly.


# Process Description

The first step of this project was to process the data. This meant reading in the different raw data files that contained the road safety data for different years, and then  merging them together into one table.

### Formatting the data
There were 5 different datasets, each containing one or more years of road safety data. The idea I had was to go through each of the 5 different datasets one at a time to get them into their own formatted table and then to join all these tables together at the end.
This was done in the *'Processing_Data.ipynb'* jupyter notebook.
This process worked fine for all of the raw data files except the 2010 second excel dataset as in this file, the cells were merged together.
I know since I completed this project, pandas has expanded its 'read_excel' function to account for merged cells but at the time, these cells were read in as merged cells so it was very difficult to deal with.
To solve this, instead of dealing with this in python, I took the more manual approach of opening this file in excel and then unmerging and filling the cells. This made it easy for when I read the data into python, however, it wasn't the most efficient process.
The process for formatting each dataset into the way I wanted it was almost the exact same for each dataset one it had been read into a pandas dataframe.
After all the data had been read in and formatted, I knew all the dataframes had a uniform layout so I could then join them together into one big dataframe.
The output of this processing was the following CSV - *'data/processed/Processed_dataframe-csv.csv'*

The *'Summary of Data Processing.ipynb'* file contains the same code as above, however, the code in this file is more compact and displayed in a summariesed fashion. Rather than going through each raw dataset seperately, in this file, I process them at the same time in steps.


### Cleaning the data
Once I had this file, I then had to move on to cleaning this data. For this, I used OpenRefine.
This involved reading the *'data/processes/Processes_dataframs-csv.csv'* into OpenRefine and from there, it was pretty easy to clean the data with this application.
There were not many errors so these were easy enough to spot especially with how easy OpenRefine is to use with its 'Text Facet' button.

The details on how I cleaned the data using OpenRefine are contained in the *'Cleaning.md'* file. This goes through the cleaning process step by step.
A CSV of the data after it had been cleaned in OpenRefine can be found at *'data/processed/Cleaned_dataframe-csv.csv'*.

As mentioned in this cleaning markdown file, I also noticed an odly large value of '1010' in the 'Total' column which I wanted to investigate further to see if I needed to change this value.
To investigate this, I opened the CSV that was expoted from OpenRefine back up in a Jupyter Notebook titled *'Analysing the cleaned dataframe.ipynb'*. Here, I compared this value with the other totals across the different years. This highlighted it as an error so I changed the '1010' to '10' as this fit with what I thought it should have been.
After this cleaning, I exported this cleaned and formatted table to the following location: *'data/processed/Final_dataframe-csv.csv'*.


### Visually analysing the data
After the data was cleaned and processed, I did some brief analysis using pandas and matplotlib in the *'Analysing the data.ipynb'* notebook. This was to help me get a better feel for the data and to understand it better for when it came to deriving proper insights from the data.

The bulk of the visual analysis of this data was then done in Plotyly through its web interface. I explored the the number of casualties by age group along with the effects seat belts have on the injury and death rates of accidents.

The following visualisation breaks down the rate of death, injury and non injury by the years, into a nice table: https://plotly.com/~nathan1/2/.
This was a summary table to use as a further base for my analysis.

I then looked at the effects seat belts have on the number of deaths, injuries and non injuries. To do this, I created the following visualisation: https://plotly.com/~nathan1/4/. Here we can see that seat belts have a clear effect on the rate of injury and death as both of these metrics are lower when the answer was 'yes' to whether the person was wearing a sea belt. This is what you would expect but it is good to verify this and be able to measure the actual affect the seat belt has.

The final piece of analysis involved breaking the casualties down by their ae group. This was th most interesting analysis piece of this project as the resutls were somewhat unusual. The visualisation can be found here: https://plotly.com/~nathan1/6/.
In this visualisation, we can see that the group with the most amount of casualties on the road is acutally the 25 to 34 year olds. I say this was unusual as if you went off insurance prices, you would expect 15 to 24 year olds to have much more casualties than the 25 to 34 year olds. While 25 to 34 year olds may be more vehicles on the road, if there are more casualties, you would still expect there also to be more crashes which would mean the insurance companies are having to pay out more to this age group.
