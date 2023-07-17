# DSIT Python Bootcamp

This repository contains the exercises and labs of the introductory Python Bootcamp of the Data Science and Information Technologies MSc program at the University of Athens. 

# Exercise 1

Write a Python script to read the DNA strings from testdna1.txt (see below) to perform the following tasks: 
- Calculate the base occurrence frequency. The file contains bases ("A", "G", "T", "C"), but also contains errors (e.g., "-", "N"). An example of the output should be like: TOTAL BASES: 100, ERRORS: 5, "A": 45, "G": 25, "T": 15, "C": 10
- Calculate the number of matches (per base) and mismatches. An example of the output should be like: A-A matches=10, G-G matches=20, T-T matches=15, C-C matches=5, mismatches=100.
    
# Exercise 2

(A) Write a Python script to run the EditDistanceM (Matrix) for all pairs (d1, d2) of DNAs, where d1 is a line in file ex2-dnalist1.txt (see below) and d2 a line in file ex2-dnalist2.txt (see below), and print the Top-10 most similar pairs (descending order).
- Based on the result of EditDistanceM, you should calculate similarity scores that should be normalised to range from 0% to 100% (100% means that the two strings are identical, 0% means that the two strings have nothing in common).
- Output example (10 lines): 1, 5, 100% 2, 3, 76.5% 3, 8, 34.6% .... where e.g., 2, 3, 76.5% means that the similarity score between the string in line 2, file ex2-dnalist1, and the string in line 3, file ex2-dnalist2, is 76.5%. Hint: use the python sort() function.

(B) Write a Python script to perform the following tasks:

- Generate 3 random base strings of length 2, 3 random base strings of length 3, 3 random base strings of length 4, ... etc, till length N, and write them to file file1.txt. N should be your choice, depending on your laptop/RAM setup. If you use large N, say 100, you may experience serious delays with the execution of EditDistance (Recursive). We suggest N=10 to start with and adjust appropriately, if needed.
- Repeat previous step, and write the base strings to file file2.txt (use same N as before). 
- Measure the execution time of EditDistanceM (Matrix) and EditDistance (Recursive) for string pairs: one string from file1.txt and one from file2.txt as follows: 1st line of file1.txt with 1st line of file2.txt, 2nd line of file1.txt with 2nd line of file2.txt, 3rd line of file1.txt with 3rd line of file2.txt etc...
- Calculate average (AVG) execution time for strings of same length.
- Plot a graph to show the performance: AVG execution time (Y-axis) vs line length (X-axis). Check here for a nice plot tutorial: https://matplotlib.org/tutorials/introductory/pyplot.html.

# Exercise 3

Download the dataset housing_california (see below or Files/Class Material/Lab4). Detailed info about the dataset can be found here. To summarise: each row represents one district. There are 10 attributes: longitude, latitude, housing_median_age, total_rooms, total_bedrooms, population, households, median_income, median_house_value and ocean_proximity. Do the following tasks:

- Run describe().
- Calculate the number of rows with null values (if any).
- Replace null values with the AVG of values in the respective column.
- Run describe().
- Replace textual values in ocean_proximity field with numeric ones. Feel free to select the text-to-number mapping (e.g., 1 for INLAND, 2 for NEAR BAY, etc…)
- Run describe().
- Plot the graphs: “median_house_value vs ocean_proximity” and “median_income vs ocean_proximity”.
- Calculate the number of rows with median_house_value > 500000.
- Calculate the number of rows with housing_median_age > 40.
- Report how much each attribute (field) correlates with the median_house_value.
- Assume that your boss did not like the solution of replacing null values with the AVG of values in the respective column (see step 3). Go back in the initial dataset and get rid of all rows with null values.
- Run describe().
