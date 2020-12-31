# The 3-billion School Improvement Grants (SIG) program has no significant effects on student outcome
In collaboration with [diegoarmaca](https://github.com/diegoarmaca) and Sharon Allman

## Summary of Findings
The objective of this analysis was to examine if there was a relationship between a school’s participation in a School Improvement Grant program and an increase in that school’s students’ achievement.  Using linear regression models, we failed to reject the null hypothesis that the SIG programs had no statistically significant effect on students’ performance over time

## Data: Data for School Improvement Grants
Data used in the analysis can be retrieved here: https://www2.ed.gov/programs/sif/index.html
The dataset sy1011-1314 includes data for four school years from 2010-11 to 2013-14. The data contains the list of schools who got the funding to implement SIG programs in each year. Year 2010-11 is implementation year 1, 2011-12 is implementation year 2, 2012-13 is implementation year 3, and 2013-14 is implementation year 4. We kept only the rows of schools who had implemented SIG models in all four implementation years. It is possible to assess the program in each implementation year. However, we choose to observe the long-term effect of the program. Therefore, the data from 2009-10 (before implementation year 1) is compared with data from implementation year 4.  

To assess the effect of the SIG program, we wanted to observe the percentage change of students in the schools that scored above proficiency in math assessment before implementation 1 (2009-10) and at implementation year 4 (2013-14). Therefore, we gathered math achievement data sets from school years 2009-10 and 2013-14 and extracted the column of math proficiency rate from each data set. The math proficiency rate has a range from 0 to 100. Moreover, the datasets contain schools that did not implement SIG programs in any of the implementation years, which allowed us to formulate a control group with random assignment method. In the end, we had a data frame observing 183 schools across 5 school years with 8 variables concerning the schools’ name, region, model implemented, math proficiency rate, and school year.      

## Method: difference-in-differences (diff-in-diff)
The method we used to estimate the effects of the SIG programs was difference-in-differences (diff-in-diff). The initial difference between the treatment and control group was taken into account. Because the SIG program only awarded the schools that ranked as low performing, the average proficiency rate in the treatment group was substantially lower than the ones in the control group— hence we did not compare the differences of proficiency rate between treatment and control group. What we wanted to compare were the changes in the treatment group over time to changes in the control group over time. 

### See the [PDF file](toronto_income_gap.pdf) for R code, data visualization and full analysis

