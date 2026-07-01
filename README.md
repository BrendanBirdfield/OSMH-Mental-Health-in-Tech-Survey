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
<img width="1919" height="1027" alt="Image" src="https://github.com/user-attachments/assets/00b43264-a30a-430b-aa7c-298967ddeb25" />
