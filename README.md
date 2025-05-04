# STATGR5293 Final Project

Authors: Peter Silverstein and Sam Gartenstein

## Project Description

The goal of our project is to understand how state-level education spending is influenced by political trifectas—situations where a single party controls the Governorship, Senate, and House of Representatives within a state. Specifically, we examine how education budgets change under unified versus divided government control across states and over time. Using data on state education per-pupil spending (adjusted to 2016 dollars) from 1997 to 2013, we employ multilevel models that account for demographic and economic factors, as well as fixed effects for state and year.

### Organization

Our `data` folder is organized as follows

  - `raw-data`: contains csv files for age and race data collected from [CDC WONDER: Multiple Cause of Death Data](https://wonder.cdc.gov/controller/datarequest/D163;jsessionid=1D7CE2ADACAB76D41155872A592E) (`demographics` folder), income data from [U.S. Census: Historical Income Tables for Households](https://www.census.gov/data/tables/time-series/demo/income-poverty/historical-income-households.html) (`income` folder), education spending data from [Urban Institute](https://datacatalog.urban.org/dataset/state-state-spending-kids-dataset), and state assembly data from [Ballotpedia](https://ballotpedia.org/Ballotpedia:Who_Runs_the_States,_Partisanship_Results,_Partisan_Control_of_State_Legislatures).
  - `processed/individual`: contains processed csv files for demographics, education spending and state assembly information, income, and unemployment
  - `processed/merged`: contains merged data used for the multilevel analysis 

 **R Files**

 - `demographic-preprocessing.Rmd` preprecesses race and age data
 - `income-preprocessingd.Rmd` preprocesses median household income data
 - `education-political-preprocessing.Rmd` preprocesses education and state political variables
 - `merging-data.Rmd` merges demographic, income, and education data for modeling
 - `educ-multilevel-models.Rmd` is our primary script for developing summary statistics and figures and running our multilevel models



### Sources

https://www.census.gov/data/tables/time-series/demo/income-poverty/historical-income-households.html

https://wonder.cdc.gov/controller/datarequest/D163;jsessionid=1D7CE2ADACAB76D41155872A592E
