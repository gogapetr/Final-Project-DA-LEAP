# Final Project DA LEAP: Understanding Student Performance

## 1. Project overview

**Project title:** Final Project Scenario 2: Understanding Student Performance  
**Course:** LEAP | Data Analytics and Statistics  
**Tools:** R, RStudio, tidyverse, ggplot2, linear regression and logistic regression

This project investigates student performance in Mathematics in Portuguese secondary education. Using data from 395 students across two schools, I carried out a data analysis workflow in R to explore which student characteristics are associated with final Mathematics grades and the likelihood of passing.

The project covers data preparation, descriptive statistics, data visualisation, contingency tables, correlation analysis, linear regression, and logistic regression. It also considers uncertainty, potential confounding factors, data limitations, and the communication of findings to a non-specialist audience.

## 2. Research questions

The analysis addresses three main questions:

1. Which student characteristics are associated with final Mathematics performance?
2. Which factors are associated with the likelihood of passing Mathematics?
3. What conclusions can reasonably be drawn from the data, and what are the limitations of the analysis?

## 3. Dataset

The project uses the **Student Performance** dataset published by the UCI Machine Learning Repository and studied by Cortez (2008).

**Dataset source:** [UCI Machine Learning Repository — Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance)

The dataset contains information collected through school reports and questionnaires. The Mathematics dataset includes 395 students and 33 variables covering demographic, family, social, educational, and academic characteristics.

Examples of variables include:

- **Demographic characteristics:** sex, age, and home address type.
- **Family and social characteristics:** parental education, family support, and relationships with friends.
- **Educational characteristics:** study time, previous class failures, school absences, and additional educational support.
- **Academic performance:** first-period grade (G1), second-period grade (G2), and final grade (G3).

### Outcome variables

The main outcome was **G3**, the final Mathematics grade, measured on a scale from 0 to 20.

A binary pass/fail variable was also created from G3, with a pass defined as a final grade of 10 or higher.

The earlier-period grades, G1 and G2, were excluded from the main predictive models because they are strongly associated with G3. Excluding them allows the analysis to focus on other student characteristics rather than relying on earlier grades to predict the final grade.

## 4. Analysis workflow

The analysis was conducted in R and followed these main stages:

1. **Data preparation:** importing the dataset, inspecting variables, checking data quality, and preparing the outcome variables.
2. **Descriptive analysis:** summarising numerical and categorical variables and examining the distributions of grades and student characteristics.
3. **Exploratory data analysis:** visualising grade distributions and comparing academic outcomes across selected student characteristics.
4. **Relationships between variables:** examining correlations, contingency tables, and pass/fail percentages across groups.
5. **Statistical modelling:** fitting a linear regression model to examine final grades and a logistic regression model to examine the likelihood of passing.
6. **Model evaluation:** examining uncertainty, residual diagnostics, predictor overlap, and limitations in model fit.
7. **Communication:** summarising the findings and their practical implications in a short presentation for an education decision-maker.

## 5. Key findings

### Academic performance

- The mean final Mathematics grade was approximately **10.41 out of 20**, with a standard deviation of approximately 4.58.
- **67.09% of students passed**, while 32.91% did not reach the passing threshold of 10.
- Students from Gabriel Pereira represented 88.35% of the sample, meaning the dataset was unevenly distributed across the two schools.

### Previous class failures

Previous class failures showed one of the clearest associations with academic performance.

- The correlation between previous class failures and final grades was approximately **−0.36**, indicating a negative relationship.
- In the linear regression model, each additional previous failure was associated with an estimated decrease of approximately **2.03 points** in the final grade, holding the other included predictors constant.
- In the logistic regression model, each additional previous failure was associated with approximately **60.1% lower odds of passing**, after adjustment for the other included predictors.

### Other findings

Sex was statistically significant in both models, with male students having higher estimated grades and odds of passing than female students in this sample, after adjustment for the other predictors.

Intention to pursue higher education was positively associated with final grades in the linear regression model, but its association with passing was not statistically significant in the logistic regression model. Study time and absences were not statistically significant predictors in either model at the 5% significance level.

These findings describe associations within the analysed sample and should not be interpreted as evidence of causal relationships.

## 6. Interpretation and limitations

Previous class failures emerged as an important indicator of subsequent academic performance in this sample. This finding suggests that students with a history of academic difficulty may benefit from early identification and appropriate educational support.

However, several limitations affect the interpretation and generalisability of the results:

- **Observational data:** the analysis identifies associations, not causal effects.
- **Potential confounding:** factors such as prior academic difficulties, motivation, family circumstances, teaching quality, and access to educational resources may influence academic performance but are not fully captured by the models.
- **Uneven school representation:** students from Gabriel Pereira account for most of the sample, so the findings may reflect this school more strongly.
- **Measurement limitations:** questionnaire-based variables may be affected by recall errors or differences in how students interpret questions.
- **Model uncertainty and fit:** the models explain only a modest proportion of the variation in final grades, and some estimates remain uncertain.
- **Limited generalisability:** findings from two schools in Portugal cannot automatically be extended to other schools, countries, or educational systems.

Statistical significance does not necessarily imply practical importance, and a non-significant result does not prove that a relationship is absent.

## 7. Presentation for education decision-makers

A separate five-slide presentation communicates the main findings to a non-specialist audience. It highlights the association between previous class failures and academic performance, discusses other findings, and explains what should not be concluded from the analysis.

**Presentation:** [Student Performance — Decision-Maker Brief](https://github.com/gogapetr/Final-Project-DA-LEAP/blob/4d2628e1662d3691696ca3032e4b98bd7d7d9f72/Presentation_DA_LEAP.pdf)

The central practical message is that previous class failures may be useful as one indicator for identifying students who could benefit from additional support. They should not be treated as a complete explanation of student performance or as a basis for labelling students.

## 8. Reflection

This project provided an opportunity to apply a complete data analysis workflow in R, from data preparation and exploratory analysis to regression modelling and communication of findings.

One of the main challenges was interpreting regression results in a way that accounts for uncertainty and avoids causal claims. Evaluating model assumptions, understanding the relationship between predictors, and distinguishing statistical significance from practical importance were also important parts of the process.

With more time, I would explore additional model specifications, investigate the influence of unusual observations, and validate the findings using data from more schools or different student cohorts. This would help assess whether the observed relationships are consistent beyond the current sample.

## 9. Project files

The repository should include the following files, where available:

- **R analysis script:** `[Link to R script](https://github.com/gogapetr/Final-Project-DA-LEAP/blob/4d2628e1662d3691696ca3032e4b98bd7d7d9f72/Final%20Project%20DA.R)`
- **Final report:** `[Link to final report](https://github.com/gogapetr/Final-Project-DA-LEAP/blob/4d2628e1662d3691696ca3032e4b98bd7d7d9f72/Presentation_DA_LEAP.pdf)`
- **Decision-maker presentation:** [Student Performance presentation](https://github.com/gogapetr/Final-Project-DA-LEAP/blob/4d2628e1662d3691696ca3032e4b98bd7d7d9f72/Presentation_DA_LEAP.pdf)
- **Dataset:** available from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance)


## Reference

Cortez, P. (2008). *Student Performance* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5TG7T