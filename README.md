# pandas-challenge
This repository contains challenge files for UT DAV Bootcamp Module 4 Data Analysis with Python

# File Notes
* PyCitySchools folder contains my solution and resource files
   * PyCitySchools.ipynb contains my written analysis in the top cell of and the complete code to output results as indicated by the instrustions.
   * Notes.docx contains my notes as I worked through the analysis including consolidating screenshots of various output results requested by the instructions and additional results from queries I temporarily added to the script. This should NOT be considered my written analysis but shows some additional query results referenced in my analysis.
   * Resources folder contains the data to be analyzed per the instructions
     * schools_complete.csv
     * students_complete.csv
* Starter_Code folder contains the filesprovided in BCS/Canvas for completing the challenge.
   


# References
The following references were used in creating the solution within the PyCitySchools folder:
 * Starter_Code\PyCitySchools\PyCitySchools_starter.ipynb leveraged for file dependencies, setup, and some code execution as well as guiding output visuals
 * removing duplicates https://blog.hubspot.com/website/duplicated-pandas

# Instructions

Setup

1. Create a new repository for this project called pandas-challenge. Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, create a folder for this homework assignment and name it PyCitySchools.
4. Add your Jupyter notebook to this folder. This will be the main script to run for analysis.
5. Push these changes to GitHub or GitLab.

Analysis Instructions

Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.
Hint: Check out the sample solution called PyCitySchools_starter.ipynb located in the .zip file to review the desired format for this assignment.

District Summary

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
Include the following:
 * Total number of unique schools
 * Total students
 * Total budget
 * Average math score
 * Average reading score
 * % passing math (the percentage of students who passed math)
 * % passing reading (the percentage of students who passed reading)
 * % overall passing (the percentage of students who passed math AND reading)

School Summary

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.
Include the following:
 * School name
 * School type
 * Total students
 * Total school budget
 * Per student budget
 * Average math score
 * Average reading score
 * % passing math (the percentage of students who passed math)
 * % passing reading (the percentage of students who passed reading)
 * % overall passing (the percentage of students who passed math AND reading)

Highest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools".

Lowest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools".

Math Scores by Grade

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Reading Scores by Grade

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Scores by School Spending

Create a table that breaks down school performance based on average spending ranges (per student).
Use the code provided below to create four bins with reasonable cutoff values to group school spending.
   spending_bins = [0, 585, 630, 645, 680]
   labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.
   spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
   spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
   spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
   spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
   overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:
 * Average math score
 * Average reading score
 * % passing math (the percentage of students who passed math)
 * % passing reading (the percentage of students who passed reading)
 * % overall passing (the percentage of students who passed math AND reading)

Scores by School Size

Use the following code to bin the per_school_summary.
   size_bins = [0, 1000, 2000, 5000]
   labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

Scores by School Type

Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".

Note: The grading rubric includes the following but it neither a part of the above instructions nor the starter notebook
 * Calculate the number of schools with math scores of 70 or higher (2 points)
 * Calculate the number of schools with reading scores of 70 or higher (2 points)
I am interpreting this as a typo intended to indicate 'NUMBER OF STUDENTS by school' rather than "number of schools". This interpretation aligns with instructions and starter code.
