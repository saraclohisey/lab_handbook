# Data Cleaning SOP
1. Understand what the quantities that have been recorded are. Use a data dictionary if one is available. Also understand what the ‘observational unit’ is in the rows. For example, does each row correspond to a single person? Or perhaps a single point in time?
2. Check data types in all columns. Change type if necessary. For example, change dates that are encoded as strings to date objects. (eg avoid having 1.0 instead of 1 if “full numbers” are required)
3. Create a list of 'acceptable' values for each column. For numerical variables this might be a range e.g. age in [0,120]. For other variables it might be a discrete set of values eg. sex in {male, female}.
4. Look at all values that are present in each column. If it is a numerical column that can take a large number of values, look at maximum and minimum values. Otherwise look at a frequency table of values.
5. Make values consistent. E.g. if there are values ‘No’ and ’NO’ in a column, set them both to ‘No’ (or however you wish to encode it).
6. Examine all values that are not ‘acceptable’. Are any due to obvious data entry errors? E.g. year is 3021 instead of 2021. If so, correct them. Are any other reasonable corrections possible? For example, perhaps a missing value for a binary variable can reasonably be taken to mean that it is 0 rather than missing.
7. Set all other values outside the acceptable range to missing
8. Check if there are duplicate rows. If so, should they be there? 
9. Are there any rows that should be combined? For example, perhaps each row corresponds to an individual, but some individuals have their data recorded in multiple rows
10. Plot distribution, ensure it follows what you expect.
11. Check column (measurement) names to ensure the data you expect is there.
12. Ensure the data is indexed. (to for example avoid duplication of parts of the dataset if in the future datasets are to be mixed – eg have a unique ID per patient)
13. Define constants for the specific dataset and ensure they are consistent for each row/patient.
14. Check for inappropriate characters (, tabs spaces)
15. Check the shape of the dataset

Variable naming
Underscores
Capital letters are BANNED :(
No numerical characters


