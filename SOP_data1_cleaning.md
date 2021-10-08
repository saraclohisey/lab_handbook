# SOP_data1_cleaning
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
date 20211008
Authors: Steven Kerr, Baillie Lab group attendees 20211006.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

# Aim
The aim of this SOP is to provide a framework for lab members to examine and clean their datasets upon receipt. 

# Method
Each dataset is unique. The recommended questions to ask about eah one are: 

[] What are the quantities that have been recorded?
  - Use a data dictionary if one is available. Also understand what the ‘observational unit’ is in the rows. For example, does each row correspond to a single person? Or perhaps a single point in time?

[] Are column (measurement) names what you expect?

[] What are acceptable values for each column? 
  - Create a list of 'acceptable' values for each column. For numerical variables this might be a range e.g. age in [0,120]. For other variables it might be a discrete set of values eg. sex in {male, female}.
  - Examine all values that are not ‘acceptable’. Are any due to obvious data entry errors? E.g. year is 3021 instead of 2021. If so can they be reasonably corrected?
  - Are any other reasonable corrections possible? For example, perhaps a missing value for a binary variable can reasonably be taken to mean that it is 0 rather than missing.
  -  Look at all values that are present in each column. If it is a numerical column that can take a large number of values, look at maximum and minimum values. Otherwise look at a frequency table of values.

[] What is the datatype of each column. 
  - Change type if necessary. For example, change dates that are encoded as strings to date objects. (eg avoid having 1.0 instead of 1 if “full numbers” are required)

[] Check for inappropriate characters (, tabs spaces)
  - Tabs
  - Spaces
  - Commas
  - Line breaks
 
[] Are values consistent in each column? 
 - If there are values ‘No’ and ’NO’ in a column, set them both to ‘No’ (or however you wish to encode it).
  
[] Can you values outside the acceptable range to missing?

[] Are there duplicate rows. 
  - If so, should they be there? 
  - Ensure the data is indexed. (to for example avoid duplication of parts of the dataset if in the future datasets are to be mixed – eg have a unique ID per patient)

[] Are there any rows that should be combined? 
  - For example, perhaps each row corresponds to an individual, but some individuals have their data recorded in multiple rows

[] Plot distribution of numerical columns, ensure it follows what you expect.

[] Define constants for the specific dataset and ensure they are consistent for each row/patient.
  - A simple example is the same patinet measured at different timepoints - is their age consistent?

[] Does the datset have a reasonable shape?
 - Are rows/columns equal all the way through. If not you may have missing data.
