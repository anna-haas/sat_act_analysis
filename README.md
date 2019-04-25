# SAT & ACT Participation Analysis

### Problem Statement

 The new format for the SAT was released in March 2016, creating a test that more closely resembles and competes with the ACT. As an employee of the College Board - the organization that administers the SAT - I am part of a team that tracks statewide participation and recommends where money is best spent to improve SAT participation rates. With two years of data available since we have implemented this new format, we would like to evaluate our progress so far and determine what step are necessary to maintain and increase participation across the United States.

---

### Executive Summary

 The SAT offered to the class of 2018 marked the second anniversary of the new SAT format. This year also marked the first time since 2012 that the SAT outperformed the ACT in terms of participation. With a nearly 25% increase in participation from 2017 to 2018, 2018 marked the highest SAT participation College Board has seen.

  While this is good news for the SAT, the ACT still holds strong power in many states. More than 15 states (majority in the Midwest) require the ACT in high school, making it difficult for the SAT to improve in these markets. Similarly, there are states that require the SAT, but the group is not as large. Recent victories in Illinois and Colorado for the SAT have boosted participation and likely play a significant role in the 2018 participation jump. To continue along this line of success it is important that College Board identifies and targets states where opportunity for ACT to SAT turnover is possible.

#### Data Collection

-  2017 ACT Data (provided and compiled by General Assembly)
-  2017 SAT Data (provided and compiled by General Assembly)
-  2018 ACT Data (provided by 2018 ACT Annual Report and compiled by me)
-  2018 SAT Data (provided by 2108 SAT Annual Report & State Reports and compiled by me)
-  ACT/SAT State Requirements (provided by the Education Commission of the States and compiled by me)

#### Exploratory Data Analysis

- Data required a bit of cleaning for incorrectly inputted data in the 2017 files we received as well as for updating data types for numerical columns
- After the 2017 data was collected and cleaned, 2018 data was manually collected as well as data relevant to state requirements. After importing this additional data, all data was combined into one table using the state as the key
- High and low participating states were examined for each test to determine any trends:
- Michigan, Delaware and Connecticut consistently experienced high SAT participation
- Wyoming, Oklahoma, Arkansas, Kentucky, Louisiana, Mississippi, Wisconsin, Montana, Nebraska, Nevada, North Carolina, Missouri, Alabama, South Carolina, Tennessee, and Utah all experienced consistently high ACT participation
- High and low scoring states were examined
- States with lower participation, had higher scores (across both tests)
- Participation YOY was examined to find states with significant participation changes (> 50%): Arkansas, Colorado, Illinois, and West Virginia
- When comparing the same test year over year the participation rate is positively correlated
- When comparing the same subject between tests to each other (e.g. ACT Math to SAT Math) the scores are slightly negatively correlated

#### Recommendations
- Continue to provide competitive and compelling bids to states considering state-mandated college-entrance exams & assessments
    - Make clear the advantages and unique value of SAT: SAT School Day, Khan Academy Free SAT Prep, value of PSAT for 10th graders, etc.
    - SAT Math & ACT Math show a weak negative relationship indicating possible differences (same for Reading)
- Continue to offer and promote SAT School Day
    - Aligns strongly with College Board's mission statement of: “We’re a mission-driven not-for-profit organization that connects students to college success
    - Reduces obstacles (time and money) to student participation
    - Can offer to individual districts (not just at the state level)
- Target states and districts that currently offer both tests at no cost to their students
    - Don't have to deal with obstacles such as legislation and money
    - States that require one test (Choice): Ohio, Oklahoma, and Tennessee
    - States that offer optional tests: DC, Hawaii, Minnesota, South Carolina

#### Next Steps
- It would be very interesting to look at the data for previous years to compare against the new data with the new SAT. It would also be helpful to have more granular information, perhaps on a district level. There are additional attributes that would be interesting to look at on the state level such as number of high school graduates, number of graduates college bound, etc.

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT/ACT|state name for associated SAT/ACT average scores and participation rates|
|2017_sat_participation|float|SAT|participation rate for the SAT in each US state in 2017 (values: 0-1)|
|2018_sat_participation|float|SAT|participation rate for the SAT in each US state in 2018 (values: 0-1)|
|2017_sat_ebrw|int|SAT|average score on reading & writing section of SAT in 2017 (values: 200-800)|
|2018_sat_ebrw|int|SAT|average score on reading & writing section of SAT in 2018 (values: 200-800)|
|2017_sat_math|int|SAT|average score on math section of SAT in 2017 (values: 200-800)|
|2018_sat_math|int|SAT|average score on math section of SAT in 2018 (values: 200-800)|
|2017_sat_total|int|SAT|average score on SAT (average of combined reading & writing + math) in 2017 (values: 200-800)|
|2018_sat_total|int|SAT|average score on SAT (average of combined reading & writing + math) in 2018 (values: 200-800)|
|2017_act_participation|object|ACT|participation rate for the ACT in each US state in 2017 (values: 0-1)|
|2018_act_participation|object|ACT|participation rate for the ACT in each US state in 2017 (values: 0-1)|
|2017_act_english|float|ACT|average score on english section of ACT in 2017 (values: 0-36)|
|2017_act_math|float|ACT|average score on math section of ACT in 2017 (values: 0-36)|
|2017_act_reading|float|ACT|average score on reading section of ACT in 2017 (values: 0-36)|
|2017_act_science|float|ACT|average score on science section of ACT in 2017 (values: 0-36)|
|2017_act_composite|float|ACT|average score on composite section of ACT in 2017 (values: 0-36)|
|2018_act_composite|float|ACT|average score on composite section of ACT in 2018 (values: 0-36)|
|act_required|string|ECS|'yes' or 'no' value indicating if a given state requires the ACT|
|sat_required|string|ECS|'yes' or 'no' value indicating if a given state requires the SAT|
   ECS = Education Commission of the States (https://www.ecs.org/wp-content/uploads/State-Information-Request_Use-of-ACT-SAT-and-PSAT-for-High-School-Testing-as-Required-by-ESSA.pdf)

### Sources:

#### DATA
* 2017 ACT Data:https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows (compiled by General Assembly)
* 2018 ACT Data: http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)
* 2017 SAT Data: https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/(compiled by General Assembly)
* 2018 SAT Data: https://reports.collegeboard.org/pdf/2018-total-group-sat-suite-assessments-annual-report.pdf
* ACT/SAT Requirements by State (ECS): https://www.ecs.org/wp-content/uploads/State-Information-Request_Use-of-ACT-SAT-and-PSAT-for-High-School-Testing-as-Required-by-ESSA.pdf

#### BACKGROUND RESEARCH
* https://www.edweek.org/ew/articles/2018/10/31/sat-scores-rise-as-number-of-test-takers.html
* https://www.princetonreview.com/college/sat-act
* https://www.chalkbeat.org/posts/co/2015/12/23/goodbye-act-hello-sat-a-significant-change-for-colorado-high-schoolers/
* https://www.chalkbeat.org/posts/co/2015/12/15/testing-giants-vie-to-provide-colorado-high-school-exams/#.Vnsoy5MrL-Y
* https://www.wsaz.com/content/news/All-WVa-high-school-juniors-to-begin-taking-SAT-exam-beginning-Spring-2018-444248263.html
* https://www.edweek.org/ew/section/multimedia/states-require-students-take-sat-or-act.html
* https://www.collegesimply.com/colleges/tennessee/the-university-of-tennessee/admission/
* https://collegereadiness.collegeboard.org/sat/k12-educators/sat-school-day
