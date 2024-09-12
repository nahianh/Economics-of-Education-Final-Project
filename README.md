# Economics-of-Education-Final-Project
This respository contains the R code I used for my Economics of Education final project: The Effects of Federal School Policing Grants on California Secondary Schools

This study tests the claim that school policing negatively affects the learning environment by leading to student detachment in the form of excessive absences and lost instructional time due to exclusionary discipline. Specifically, I investigate the impacts of receiving a federal school policing grant on the chronic absenteeism and suspension rates of California public middle and high schools. Leveraging data on agencies who applied for a COPS Hiring Program (CHP) grant between 2014-2017, I identify a set of treated schools that received the grant and a set of untreated schools whose applications were rejected through propensity score matching. Conducting a paired t-test to estimate the mean sample differences in the chronic absenteeism and suspension rates, I find statistically significant evidence that schools receiving the grant experienced higher suspension rates. However, I do not find evidence to suggest that the CHP grant impacts chronic absenteeism. 

![](https://github.com/nahianh/Economics-of-Education-Final-Project/blob/main/146plot1_s.png?raw=true)
![](https://github.com/nahianh/Economics-of-Education-Final-Project/blob/main/146plot2.png?raw=true)


My analysis relies on agency-level data obtained via a FOIA request to the COPS office. The approved request included information on the application year, award status, and Originating Agency Identifier (ORI) numbers for all 101 California agencies that applied for a CHP grant for school-based policing between 2014 and 2020. According to the FOIA request response, the COPS office was unable to locate applications prior to 2014, despite the program’s onset in 2006. Using the publicly released applicant ranking documents available on the COPS website, I appended the application scores to this data. 

To match these agencies to schools, I began by linking the ORI numbers to the corresponding Federal Information Processing Standards (FIPS) county codes.  Using the FIPS codes, I then matched the agencies to their corresponding school districts.  Finally, I used the unique district codes to merge in individual schools, excluding those serving students outside middle or high school age, special needs facilities, correctional and juvenile detention centers, online programs, and vocational schools.  Doing so will allow for more accurate comparisons of the effects on public secondary schools. Because the agencies require time to recruit, hire, and place SROs after receiving a grant, I estimate the effects for the school year that follows the application year. I thus merged in data on chronic absenteeism, suspensions, student demographics, and total enrollment from 2015-2018 from the CDE.  As the CDE did not have chronic absenteeism data available for the 2015-2016 school year, I obtained this data from the CRDC.  After removing agencies who received the grant in multiple years, I then combine the data across the four years into one dataset, allowing for a larger sample size. 

