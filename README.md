# School_District_Analysis

## Purpose 
Initially, this prpject was looking at the differnces in the 9th-12th grades across 15 different high schools to see how the school's budget, school type, and size were affecting the success of the students when it came to reading and math scores. However, we were later informed that the initial dataset was inaccurate due to issues with the scores reported for  Thomas High School's 9th graders. So, we were tasked with rexamining the data, but with having that problem group removed. This was accomplished by setting the values of that group to NaN's, so they wouldn't affect the overall averages.

    student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th") , "math_score"] = np.nan
    student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th") , "reading_score"] = np.nan
## Results
  * To start the overall district summary was barely affected. There was slight drop in the percentange of students passing math, reading, and overall, but the change would not change any major decisions. 
  * The individual school summary is where you see the first major differnce in the data as we can focus specifically on Thomas High. Originally the passing percentages were 93%, 97%, and 90% for math, reading, and overall passing respectively. However, after dropping the 9th grade scores, the percentages dropped significantly.
        
        School Type  Total Students Total School Budget Per Student Budget Average Math Score Average Reading Score  Passing Math  Passing Reading Overall Passing
        Thomas High School 	Charter 	1635 	$1,043,130.00 	$638.00 	83.350937 	83.896082 	66.911315 	69.663609 	65.076453 
  * With this change Thomas High School went from being a contender for the best school in the district, to not even breaking out of the bottom half of the schools.
  * Much like the district summary, the scores by grade weren't greatly affected by the change in the data. This a due to there being 14 other 9th grades that absorbed the impact of Thomas High being taken out.
  * The scores based on spending is where you start to see more of a difference. Thomas High fell under the $630-$644 spending and there were only three other schools in that category. Here the biggest change was in the percent reading scores, which dropped from 94% to 92%.
  * For the school size, there didn't appear to be any significant change in any of the percentages after removing the Thomas High 9th grede data.
  * Lastly, for school type, Thomas High fell under the charter category and like the school size, there was no significant change in the data. 

## Summary

Overall, there are four categories that have been affected by removing Thomas High School's 9th grade scores from the dataset: Average Math Scores, Average Reading Scores, % Passing Math, and % Passing Reading. Due to there being 14 other schools present in the dataset, this change has difficulty being seen unless you are specifically lookings at Thomas High's results and even when you this, results like overall passing aren't affected greatly, as the 10th-12th data picks up the slack.

	
