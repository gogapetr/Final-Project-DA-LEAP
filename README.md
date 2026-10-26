Final-Project-DA-LEAP

A short README, introduction or portfolio page explaining the project and 
linking the files

1. Project title and scenario. 

Project title: 

Final Project Scenario 2: Understanding Student Performance

Description: 

Using a real dataset about student performance in secondary 
education, I will carry out a complete data analysis workflow in R. 
The project will include descriptive statistics, visualisation, contingency 
tables, correlation, linear regression and logistic regression. A discussion on 
uncertainty,causality, limitations will be included and on how the results 
should be communicated to a non-specialist audience.

2. Research question.

The present project will be using the Mathematics-course dataset and aims to 
explore: 
a. which student characteristics are associated with final Mathematics 
   performance, 
b. which factors are linked to the risk of failing, and 
c. what conclusions can reasonably be drawn from the data?

3. Data. 

This data approach student achievement in secondary education of two Portuguese 
schools. The data attributes include student grades, demographic, social and 
school related variables and it was collected by using school reports and
questionnaires. The dataset comes from a study by Cortez (2008) and this is link
to the dataset page:https://archive.ics.uci.edu/dataset/320/student+performance
 
Variable information:
1 school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - 
  Mousinho da Silveira)
2 sex - student's sex (binary: 'F' - female or 'M' - male)
3 age - student's age (numeric: from 15 to 22)
4 address - student's home address type (binary: 'U' - urban or 'R' - rural)
5 famsize - family size (binary: 'LE3' - less or equal to 3 or 
  'GT3' - greater than 3)
6 Pstatus - parent's cohabitation status (binary: 'T' - living together or
  'A' - apart)
7 Medu - mother's education (numeric: 0 - none,  1 - primary education 
  (4th grade), 2 “ 5th to 9th grade, 3 “secondary education or 4
  “higher education)
8 Fedu - father's education (numeric: 0 - none,  1 - primary education 
  (4th grade), 2 “ 5th to 9th grade, 3 “secondary education or 4 
  “higher education)
9 Mjob - mother's job (nominal: 'teacher', 'health' care related, 
  civil 'services' (e.g. administrative or police), 'at_home' or 'other')
10 Fjob - father's job (nominal: 'teacher', 'health' care related,
   civil 'services' (e.g. administrative or police), 'at_home' or 'other')
11 reason - reason to choose this school (nominal: close to 'home', 
   school 'reputation', 'course' preference or 'other')
12 guardian - student's guardian (nominal: 'mother', 'father' or 'other')
13 traveltime - home to school travel time (numeric: 1 - <15 min.,
   2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
14 studytime - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours,
   3 - 5 to 10 hours, or 4 - >10 hours)
15 failures - number of past class failures (numeric: n if 1<=n<3, else 4)
16 schoolsup - extra educational support (binary: yes or no)
17 famsup - family educational support (binary: yes or no)
18 paid - extra paid classes within the course subject  
   (binary: yes or no)
19 activities - extra-curricular activities (binary: yes or no)
20 nursery - attended nursery school (binary: yes or no)
21 higher - wants to take higher education (binary: yes or no)
22 internet - Internet access at home (binary: yes or no)
23 romantic - with a romantic relationship (binary: yes or no)
24 famrel - quality of family relationships (numeric: from 1 - very bad to 
   5 - excellent)
25 freetime - free time after school (numeric: from 1 - very low to 
   5 - very high)
26 goout - going out with friends (numeric: from 1 - very low to 5 - very high)
27 Dalc - workday alcohol consumption (numeric: from 1 - very low to
   5 - very high)
28 Walc - weekend alcohol consumption (numeric: from 1 - very low to
   5 - very high)
29 health - current health status (numeric: from 1 - very bad to 5 - very good)
30 absences - number of school absences (numeric: from 0 to 93)

# these grades are related with the course subject:
31 G1 - first period grade (numeric: from 0 to 20)
31 G2 - second period grade (numeric: from 0 to 20)
32 G3 - final grade (numeric: from 0 to 20, output target)

Important note: the target attribute G3 has a strong correlation with 
attributes G2 and G1. This occurs because G3 is the final year grade 
(issued at the 3rd period), while G1 and G2 correspond to the 1st and 
2nd period grades. It is more difficult to predict G3 without G2 and G1,
but such prediction is much more useful

4. Analysis workflow. 
Summarise the main steps in R: preparation, exploratory analysis, 
relationships and statistical modelling.


5. Key results. 
Show the most important statistics, plots and model results. Do not 
reproduce all R output.


6. Interpretation and limitations. 
Explain what the results mean, how certain the conclusions are, 
and what cannot be concluded. Include causality, confounding and 
practical importance where relevant.


7. Decision-maker presentation.
Include or link to your short non-specialist presentation of 
the main findings, practical meaning, uncertainty and limitations.


8. Reflection. 
Briefly explain what you learned, what was difficult and what you 
would improve with more time