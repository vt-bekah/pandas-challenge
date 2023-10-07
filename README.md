# pandas-challenge
For this project, I take on the role of a data scientist for a school district to analyze their data consisting of type (District vs. Charter), budget, student population size, student gender, math and reading scores. My goal is to identify trends and correlations

# Features
* Create a high-level snapshot of the entire district with key metrics in a dataframe:
   * number of unique schools; total students; total budget
   * average math score; average reading score
   * % passing math (the percentage of students who passed math)
   * % passing reading (the percentage of students who passed reading)
   * % overall passing (the percentage of students who passed math AND reading)
* Create a summary by school that includes the following:
   * school name; school type; total students; total school budget; per student budget 
   * average math score; average reading score
   * % passing math (the percentage of students who passed math)
   * % passing reading (the percentage of students who passed reading)* 
   * % overall passing (the percentage of students who passed math AND reading)
* Identify highest-performing & lowest-performing schools by overall passing rateSchool name
* Display math and reading scores by grade
* Display scores by school spending including average math score, average reading score, % passing math, % passing reading, % overall passing
* Display scores by school size
* Display scores by school type


# Results
Within this population, Charter schools have notably better math scores, passing math rates, passing reading rates, and overall passing rates when compared to District schools. Charter school success correlates to smaller school size and smaller per student budgets. However, there are some indicators theese are not relationships of causation:
    - there is one large Charter school in which its performance is aligned with the rest of the Charter schools rather than District schools of that size
    - there is one District school that has a lower per student budget in which its performance is aligned with the rest of the District schools rather than the Charter schools of similar budget per student. 

While average math scores vary across schools (7.2 points different between maximum and minimum values), they are consistent across grade levels within a school regardless of school type. The difference between maximum and minimum math scores within a school across grade levels ranges from 0.3 to 2.2 points. Averaging all the differences (max - min) across schools results in 1 point. Evaluating this led me to wonder if student population changes were correlated. I made an assumption that a headcount snapshot across grade levels would align with headcount changes of a single class progressing from 9th to 12th grade and created a groupby.count() with some additional analysis in Excel (screenshot of additional groupby and excel calculations is the last image in Notes.docx). While population by grade level decreases by 27 % to 35% (depending on the school) from 9th grade to 12th grade, there does not appear to be a trend related to scores nor school type. Additional conclusions may be drawn from following a class population from 9th to 12th grade including noting transfers and performance.

Future analysis will include a deeper statistical look. There appears to be a bimodal disrtibution within the math scores when looking at the compare of average math scores and passing math rates between District and Charter schools. Charter school average math scores are 83.5 with District school average math scores 77 creating a difference of 6.5 points. The percent passing math for Charter scools is 93.6% while with the District rate at 66.5% with a difference of 27.1%. With the average scores closer than the passing rates, there is difference in variation which could lead to other avenues to identify focus areas for future improvement.


# File Notes
* PyCitySchools folder contains my solution and resource files
   * PyCitySchools.ipynb contains my written analysis in the top cell and the complete code to output results as indicated by the instrustions in the following cells.
   * Notes.docx contains my notes as I worked through the analysis including consolidating screenshots of various output results requested by the instructions and additional results from queries I temporarily added to the script. This should NOT be considered my written analysis but shows some additional query results referenced in my analysis.
   * Resources folder contains the data to be analyzed per the instructions
     * schools_complete.csv
     * students_complete.csv
* Starter_Code folder contains the files provided in BCS/Canvas for completing the challenge.

    

# References
The following references were used in creating the solution within the PyCitySchools folder:
 * Starter_Code\PyCitySchools\PyCitySchools_starter.ipynb leveraged for file dependencies, setup, and some code execution as well as guiding output visuals
 * removing duplicates https://blog.hubspot.com/website/duplicated-pandas


# Getting Started

## Prerequisites
You must have an environment with python 3.10+, jupyter notebook, and pandas to execute the notebook (PyCitySchools.ipynb)

## Cloning Repo
$ git clone https://github.com/vt-bekah/pandas-challenge.git

$ cd pandas-challenge

$ jupyter lab

# Built With
* Python v3.10.11
* jupyter notebook v6.5.2
* jupyterlab v3.6.3
* conda v23.5.0

**Python Modules**
* pandas v1.5.3

