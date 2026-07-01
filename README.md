# OSMH-Mental-Health-in-Tech-Survey
An interactive report made in power BI looking at Mental Health in the tech industry. Various factors were assessed, including comparison of mental health in various countries. Employers attitudes at approaches to mental health such as mental health care coverage and employees willingness to discuss mental health issues with supervisors.


Data was downloaded for each year of the OSMH mental health in tech survey: https://osmhhelp.org/research.html.
This data was then processed in python. Each years survey was loaded as a csv. A selection of survey questions were selected and each column name representing each question was processed to be consitent in format. 
Each years survey data was then joined into a single a csv.
The rows of each column were processed including string reformatting, removing missing values and filling missing values with logical replacement values. Unlikely age values those under 18 and over 100 were removed.
The answers from the survey question  'do you believe you have a mental health condition' were used to conditionaly replace the missing values of "Do you believe your productivity is ever affected by a mental health issue?"
with either no if they answered yes to having a mental health condition or not applicable to me if they answered yes.

Data was then loaded into power BI to answer questions from the data including: Has employers handling of mental health improved over time as rated by employees? How many working hours were lost due to poor mental health?
As well as showing demographic differences in mental health between facotrs such as gender, age and location. 

The first page of the report looks at general demographic patterns with mental health. Including comparison of average age of having a self identified mental health disorder and proportion of people with a mental health disorder for different genders and work locations. 
Stand out findings include a high proportion of people identified as trans-male and trans female has a mental health disorder compared to those identified as men and women.
There was also a high proportion of people with mental health disorders among developing countries such as Cameroon, Ecuador and Guatemala among others. However this finding could be skewed by a small sample size for individual countries. This is looked at further in the 4th page comparing mental health between MEDC and LEDC countries. 
<img width="1919" height="1029" alt="Image" src="https://github.com/user-attachments/assets/84124db9-203c-479b-9d5c-577d910db6d6" />

The second page focuses on how employers approaches to mental health have changed over time and comparisons of business size on these approaches. This included mental health care coverage, providing mental health resources and how comfortable employees felt approaching their direct supervisors about their mental health concerns.
Mental health care coverage seemed to peak around 2018 and drop off around 2020, although this is not an exact measure of employers mental health care coverage as all values are self reported from employees. 
How comfortable employees felt going to supervisors with mental health concerns also dipped around 2020. This potentially could be impacted by covid as more employees work from home and had less face to face contact with their supervisors. 

Employees from larger businesses rated their companies as providing more helath care coverage and resources than those from smaller businesses. This makes sense as large companies have more resources to allocate however employees from the largest businesses (1000+ employees) had the lowest rating of comfort going to supervisors with mental health concerns. Both findings suggest that a lack of personal and interpersonaly connected approaches to mental health care should be considered not just the amount of resources allocated to mental health expecially for larger businesses.
<img width="1919" height="1032" alt="Image" src="https://github.com/user-attachments/assets/7f2fb18c-b762-4ce8-9c37-0e3a104c04c1" />

The third page looks at the percentage of the work day that is lost to mental health for each years survey and the number of hours per day that are lost to poor mental health for each gender.
A measure was created to calcualte estimates of hours wasted from the survey question 'what percentage of the work day was lost to poor mental health' Answers ranges from 1-25% up to 76-100% 
These lower and upper bounds were converted in to upper middle and lower estimates of hours wasted per day.
The most notable finding from this page is that men with mental health issues rated losing a much higher percentage of the work day to poor mental health than other genders with meental health issues. This could be explained by the differences in which men and women process mental health issues many surveys show that men tend to externalise their problems indicated by higher rates of suicide and outwards projected behaviour such as violence, where as women tend to internalise their mental health problems looking inward with more internaly directed behaviours. This potentially could explain these differences. 
Another potential link to the effect of the pandemic on mental health can be seen as the percentage of the work day lost to mental health peaks around 2020. This coincides with an increase in working from home during the pandemic and many studies have shown the pandemic exacerbated mental health issues.
<img width="1919" height="1032" alt="Image" src="https://github.com/user-attachments/assets/c0405eec-e987-491f-8246-607493c6da33" />
