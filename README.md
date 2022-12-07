# Visualization of DC's K-12 Education Finance Disparities under the Impact of COVID


## Research Question 
We will evaluate the impact of financial disparities on test scores in K-12 schools in Washington D.C. before and after the COVID-19 pandemic. We want to find out whether students' academic performances been affected by the varying levels of financial support that each school can apply.    
We hypothesize that a school's level of spending plays a factor in how much test scores varied; meaning that the more resources the school was able to provide, the less the math and reading scores dropped from 2019 to 2021.


## Data Sources [(Google Drive)](https://drive.google.com/drive/folders/1Qk-ejtFRSZE5vp1_clnRzBpCVDkI11X6?usp=sharing)
- For measuring students' academic performances we use [NAEP data](https://www.nationsreportcard.gov/ndecore/landing)
- For school spending data we use [Edunomics Lab data](https://edunomicslab.org/nerds-download/)
- For demographic data of children and parents we use [NCES data](https://nces.ed.gov/programs/edge/TableViewer/acsProfile/2019)
- For geographic data of school district we use [Census data](https://www.census.gov/programs-surveys/sdrp/updates/school-district-boundaries.html)


##  Points of Research Interest
- [ ] Which DC schools had the biggest drop-offs from 2019 to 2022?
- [ ] Where were students best able to adapt to online learning?
- [ ] How the family income levels and the financial disparities among schools contribute to students' adaptability to online learning? 
- [ ] How the pandemic impact differently on DC's public schools and charter schools? 

## google doc : https://docs.google.com/document/d/1OqDUkqvDUaNT7UChBlY2vDq3t-FQkgKKANqsNfVpwvc/edit#

## Notebooks 

00_ pullNCESdata: https://github.com/shiuanC/final_team7/blob/main/code/00_pullNCESdata.ipynb
- [ ] takes in an excel file containing the various school's financial data form 2018-2019 and 2019-2020 
- [ ] uses nces_process function to clean the two datasets
- [ ] merges the two academic year dataframes into one nces dataframe
- [ ] calculates the percentage change in per pupil expenditure from 2018-2019 to 2019-2020
- [ ] returns clean csv dataframe called nces

01_pullSTARdata: https://github.com/shiuanC/final_team7/blob/main/code/01_pullSTARdata.ipynb
- [ ] takes in an excel file containing data on each school's STAR reports from 2018-2019 and 2019-2020
- [ ] cleans column names
- [ ] merges the two academic year dataframes into one star dataframe
- [ ] calculates the percentage change in STAR score from 2018-2019 to 2019-2020
- [ ] returns clean csv dataframe called star

02_pullDiversityData: https://github.com/shiuanC/final_team7/blob/main/code/03_PullDiversityData.ipynb
- [ ] takes in an excel file containing data on student background's, msot importantly the percentage of student's deemed "at-risk", from 2018-2019 and 2019-2020
- [ ] gives each school a label on a scale of 1-5 according to risk percentage 
- [ ] schools labeled 1 having a small number of "at-risk" students and schools labeled 5 having a lot of "at-risk" students
- [ ] returns clean csv dataframe called diversity 

03_MergeDataframes: https://github.com/shiuanC/final_team7/blob/main/code/04_MergeAllDataframes.ipynb
- [ ] takes in nces, star, and diversity csv files 
- [ ] merges the dataframes together on school code 
- [ ] only keeps school's that has both STAR and NCES data 
- [ ] cleans columns 
- [ ] returns clean csv file called all_df
    
04_DescriptiveFigs: https://github.com/shiuanC/final_team7/blob/main/code/05_DescriptiveFigs.ipynb
- [ ] takes in all_df csv file 
- [ ] returns plot of percentage of at risk students against total per-pupil ecxpenditures
- [ ] returns plot of change in STAR scores against change in per puil expenditures by percentage of "at-risk" students 
- [ ] returns plot of the change in per puil expenditure and change in STAR score for each DC public school 
- [ ] returns plot of average change in STAR score for each ward 
- [ ] returns plot of average change in STAR score and average per-pupil expenditure for each ward 
- [ ] returns plot of each school's STAR score, per-pupil expenditure, at-risk percentage, and enrollment size 
- [ ] returns seperate geoplots for each school's STAR score and per-puil expenditure 

05_CorrelationRegression: https://github.com/shiuanC/final_team7/blob/main/code/06_CorrelationRegression.ipynb
- [ ] takes in all_df csv file 
- [ ] uses an ols regression model to see the effect of per-pupil expenditures STAR score
- [ ] returns summary table of regression findings

