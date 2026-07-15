# OSMH-Mental-Health-in-Tech-Survey

***Summary:***

An interactive report made in Power BI showing results from multiple years of the OSMH Mental Health in Tech survey. Data was downloaded from OSMH mental health site multiple years of data was cleaned and joined in python and then imported into Power BI. To focus the project a subset of questions were visualised and pages focussing on 4 key areas were created: 
- Demographic differences in mental health: age, gender and location
- Employers attitude and approaches to mental health including factors like mental health care coverage, resources provided to support employees mental health and employees willingness to speak to supervisors about mental health concerns
- How much work time was lost to poor mental health both proportionaly and how many hours per day were lost between factors like gender changes overtime
- Differences in mental health between LEDC and MEDC countries


***Data Collection and Processing: Python:***

Data was downloaded as a csv for each year of the OSMH mental health in tech survey from: https://osmhhelp.org/research.html.
This data was then imported and processed in python. Each year's survey was loaded as a seperate CSV. A selection of survey questions were selected and each column name representing each question was processed to be consitent in format because some of the same questions were reworded over several years. 
Each years survey data was then joined into a single CSV.
The rows of each column were processed including string reformatting, removing missing values and filling missing values with logical replacement values. Unlikely age values, (under 18 and over 100) were removed.
The answers from the survey question  'do you believe you have a mental health condition' were used to conditionaly replace the missing values of "Do you believe your productivity is ever affected by a mental health issue?"
If there was a missing value in the productivity question and they answered 'no' to having a mental health condition then the missing value was replaced with 'not applicable to me' if they answered 'yes' to having a mental health condition then "no" was used as the answer to the productivity question.


***Data Visualisation: Power BI***

Data was then loaded into power BI to answer questions from the data including: Has employer's handling of mental health improved over time as rated by employees? How many working hours were lost due to poor mental health?
Demographic differences in mental health between factors such as gender, age and location were also assessed. 

For the page on the effects of poor mental health in productivity, a measure was created to calculate estimates of hours wasted. The survey question 'what percentage of the work day was lost to poor mental health' was used to estimate the total hours lost to poor mental health per day. Answers ranged from 1-25% up to 76-100%.
These lower and upper bounds were converted in to upper, middle and lower estimates of hours wasted per day. This was done by creating conditional columns multiplying 8 hours as an assumed average work day by the lower bound numbers in one column and the upper bounds in another. For example a response of 1-25% wasted work day would be converted into 8*0.01 (0.08) for the lower column and 8*0.25(2) for the upper column.


**1.Demographic Differences**

This report page looks at general demographic patterns with regard to mental health. Comparison of average age of having a self identified mental health disorder and proportion of people with a mental health disorder for different genders and work locations. 
Stand out findings included a higher proportion of people identified as trans-male and trans female having a mental health disorder compared to those identified as men and women.
There was also a high proportion of people with mental health disorders among developing countries such as Cameroon, Ecuador and Guatemala among others. However this finding could be skewed by a small sample size for individual countries. This is looked at further in the 4th page comparing mental health between MEDC and LEDC countries. 
<img width="1919" height="1029" alt="Image" src="https://github.com/user-attachments/assets/84124db9-203c-479b-9d5c-577d910db6d6" />


**2.Employers Approach to Mental Health**

How employer's approaches to mental health have changed over time and comparisons of business size and these approaches. This included mental health care coverage, providing mental health resources and how comfortable employees felt approaching their direct supervisors about their mental health concerns.
Mental health care coverage seemed to peak around 2018 and drop off around 2020, although this is not an exact measure of employers mental health care coverage as all values are self reported from employees. 
How comfortable employees felt going to supervisors with mental health concerns also dipped around 2020. This potentially could be impacted by covid as more employees worked from home and had less face to face contact with their supervisors. 

Employees from larger businesses rated their companies as providing more health care coverage and resources than those from smaller businesses. This makes sense as large companies have more resources to allocate however employees from the largest businesses (1000+ employees) had the lowest rating of comfort going to supervisors with mental health concerns. Both findings suggest that a lack of personal and interpersonaly connected approaches to mental health care should be considered not just the amount of resources allocated to mental health, especially for larger businesses.
<img width="1919" height="1032" alt="Image" src="https://github.com/user-attachments/assets/7f2fb18c-b762-4ce8-9c37-0e3a104c04c1" />


**3. Impact of Mental Health on Productivity**

This page looks at the percentage of the work day that is lost to mental health for each years survey and the number of hours per day that are lost to poor mental health for each gender. 
The most notable finding from this page is that men with mental health issues rated losing a much higher percentage of the work day to poor mental health than other genders with mental health issues. This could be explained by the differences in which men and women process mental health issues many studies show that men tend to externalise their problems indicated by higher rates of suicide and outwards projected behaviour such as violence, where as women tend to internalise their mental health problems looking inward with more internally directed behaviours. This potentially could explain these differences. 
Another potential link to the effect of the pandemic on mental health can be seen as the percentage of the work day lost to mental health peaks around 2020. This coincides with an increase in working from home during the pandemic and many studies have shown the pandemic exacerbated mental health issues.
<img width="1919" height="1032" alt="Image" src="https://github.com/user-attachments/assets/c0405eec-e987-491f-8246-607493c6da33" />


**LEDC vs MEDC Countries**

Here mental health between MEDC and LEDC countries was compared. Groups were created within power BI to seperate countries into MEDC and LEDC these were then used to compare proportion of employees with mental health disorders and mental health care coverage and percentage of work day lost. 
The most interesting finding shows that whilst MEDC countries showed higher rates of mental health disorders, LEDC countries showed a higher percentage of wasted work day to mental health problems. This may be due to employees from MEDC countries having better access to mental health care coverage allowing them to better manage their mental health disorders and those disorders being less disruptive to their work and life.
A strong lesson can be taken from this that companies providing mental health care coverage and support can potentially improve the productivity of their workers. 
<img width="1919" height="1029" alt="Image" src="https://github.com/user-attachments/assets/b4bbf9da-e767-4cb2-8faa-90ebba8515d9" />
