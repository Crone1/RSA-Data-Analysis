1.  I converted the processed dataframe to a CSV file within the processing notebook so that I could open it in OpenRefine.
    This file is in the data/processed directory under the name 'Processed_dataframe-csv.csv'.

2.  When I opened this file in OpenRefine, I went through each column of the table created from the CSV to explore the text facet of each, column to spot and clean errors. The errors that I spotted were as follows:

    - Some results in the 'Sex' column were just the first letter of the gender name ('M' or 'F'), while others were the full gender name ('Male' or 'Female'). To solve this I changed the attributes with only the first letter of the gender name so that they were the full gender name.

    - There was a spelling mistake of the 'Age unknown' attribute in the 'Age' column, so I changed these small few 'Age uknown' attributes so that they were spelled correctly.

    - There was a string value 'None' in the 'Total' column which I changed to 0 instead to match the other integer type attributes.

    - I also noticed that there was a value '1010' for the number of male pedal cyclists between the age of 55 and 64 years killed in the year 2011. I thought this was an outlier but wasnt 100% sure so decided to do a comparison of this value with the other values back in the notebook. I saved that file from OpenRefine as 'Cleaned_dataframe-csv.csv' in the data/processed directory. I then opened it in the notebook 'Analysing the cleaned dataframe' where I compare it with the other totals, and the totals of rows with these same attributes in other years. After doing this, I saw that this value must clearly be wrong so decided to change it to the value '10'. I decided upon '10' as '1010' is made up of two "10"'s and I thought that this is the most reasonable explination for such an outlier. I figured the person must have just entered the value twice accidentally.

3.  I also cleaned some errors within the data within the processing phase. These errors include:

    - Spotting that a column in the 2010 dataset was misspelled like 'Cassualties Injured (Number)' instead of 'Casualties Injured (Number)'. The misspelling of this column didn't affect me as I was going to change this column name anyways.

    - Changing a value in the same column as in the above point from '1.3' to '13' as this value had to be a whole number and I felt that the number '13' was the most likely value that this value was meant to be.

4.  The formats of the initial datasets were also cleaned during the processing along with fixing of many other minor issues in the datasets. Examples of this is are:

    - Changing the numbers in the 'Age' column from single digit numbers to double digit numbers so that they could be sorted easily.

    - Changing the type of the column 'Total' for injured casualties in the 2010 dataset from float to integer.
        
