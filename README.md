# PyCity School District Analysis
## Project Overview

Throughout this module, we worked with Maria, who guided us through building an analysis of PyCity high school data. After analyzing the data based on a number of different parameters, Maria learned of evidence that the test scores for 9th graders at Thomas High School had been tampered with. Since it would not be possible to fairly determine whether or not certain scores for specific individual students were affected, the only course of action would be to eliminate the scores for all the students in grade 9 at that school from our dataset. Maria asked that we filter out those students' data and re-run the analysis for the whole district without them.

### Resources

- Data sources: clean_students_complete.csv, schools_complete.csv
- Software: Python 3.7, Anaconda command line client 1.9.0, Conda 4.13.0, Jupyter Notebook 6.4.8

## Results
### Impact on District Summary

![Original_District_Summary](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/district_summary_original.png)

This is the original district-level summary, before excluding the data from Thomas High School 9th graders.

![Updated_District_Summary](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/district_summary_updated.png)

This is the updated district-level summary, with the Thomas High School 9th grade test scores removed from the dataset. Changes for the district-wide summary include:
- Average Math Score changed from 79.0 to 78.9
- % Passing Math changed from 75.0% to 74.8%
- % Passing Reading changed from 85.8% to 85.7%
- Overall Passing % changed from 65.2% to 64.9%

### Impact on School Summary

![Original_School_Summary](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/school_summary_original.png)

This is the original summary of results for each school, before excluding the data from Thomas High School 9th graders.

![Updated_School_Summary](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/school_summary_updated.png)

This is the updated summary of results for each school, with the Thomas High School 9th grade test scores removed from the dataset. Changes to the summary for Thomas High School include:
- Average Math Score changed from 83.42 to 83.35
- Average Reading Score changed from 83.85 to 83.90
- % Passing Math changed from 93.27% to 93.19%
- % Passing Reading changed from 97.31% to 97.02%
- % Overall Passing changed from 90.95% to 90.63%

### Impact on Thomas High School's Performance

![Original_Top_5_Schools](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/top5_original.png)

These are the original rank-order results of the five top-performing high schools in the district based on the Overall Passing % metric, before excluding the data from Thomas High School 9th graders.

![Updated_Top_5_Schools](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/top5_updated.png)

These are the updated rank-order results of the five top-performing high schools in the district based on the Overall Passing % metric, with the Thomas High School 9th grade test scores removed from the dataset. Changes to the results for Thomas High School are the same as those listed in the school summary above; as can be seen in these two images, Thomas High School remained the second-ranked school in the district even after the updated score calculations.

### Impact on Subdivided District-Level Analyses

![Original_Math_Scores_by_Grade](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/math_by_grade_original.png)
![Updated_Math_Scores_by_Grade](https://github.com/tfish110/School_District_Analysis/blob/main/Resources/math_by_grade_updated.png)

A number of analyses were conducted which broke down the testing data for the district by several other parameters. Above are images of the breakdown of scores for each school by grade level. Since 9th grade scores at Thomas High School were the only ones eliminated from the dataset, that is the only change reflected here. There were also district-wide comparisons of schools' scores based on three other categories: school budget per capita (divided into four roughly equal spending categories), student population (divided into "small," "medium," and "large" schools), and school type (district vs. charter). Eliminating the 9th grade scores from Thomas High School did not result in any changes to the these district-wide comparisons.

## Summary

Overall, eliminating the scores for 9th grade students at Thomas High School had very little impact on the district's analysis.

As is outlined in the results above, Thomas High School's own school-wide averages and passing rates saw only minor changes after eliminating the 9th grade scores, on the order of less than a few tenths of a point or tenths of a percent for each test score metric. This must mean that the scores for the 9th grade students did not vary significantly from those of the rest of Thomas High School's population. If there was indeed academic dishonesty in an attempt to artificially inflate the 9th grade scores, this would suggest that it was likely isolated to a small number of students. Interestingly, the reading score average actually increased slightly after eliminating the 9th grade scores, further suggesting a minimal impact of the grade tampering.

Similarly, the district-wide averages were barely changed by eliminating the suspicious data. As the 9th graders for one particular school are an even smaller subset of the district as a whole, it's expected that the minor impact on that one's school scores would be even less impactful on the scale of the whole district. That narrative clearly holds up in the data outlined above. Beyond the minor changes of fractions of a point or fractions of a percent that the district-wide summary saw, the fact that several of the other analyses did not change at all after removing the Thomas High School 9th grade data highlights the insignificance of the removal.

The only caveat would be that sometimes, fractions of a point or a percentage point can make a difference in certain contexts. For example, the district-wide overall passing rate changed from 65.2% to 64.9%. While that is a very small change, it could have a big impact if acheiving a minimum passing rate of 65% was a threshhold for state or federal funding for the district. That could very easily lead to an ethical conundrum if the school board is left to choose whether or not to include potentially corrupted data in their analysis.
