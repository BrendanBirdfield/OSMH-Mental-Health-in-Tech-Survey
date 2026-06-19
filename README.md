# OSMH-Mental-Health-in-Tech-Survey
An interactive report made in power BI looking at Mental Health in the tech industry. Various factors were assessed, including comparison of mental health in various countries. Employers attitudes at approaches to mental health such as mental health care coverage and employees willingness to discuss mental health issues with supervisors.


Data was downloaded for each year of the OSMH mental in tech survey: https://osmhhelp.org/research.html.
This data was then processed in python. Each years survey was loaded as a csv. A selection of survey questions were selected and each column name representing each question was processed to be consitent in format. 
Each years survey data was then joined into a single a csv.
The rows of each column were processed including string reformatting, removing missing values and filling missing values with logical replacement values for. Unlikely age values those under 18 and over 100 were removed.
The answers from the survey question  'do you believe you have a mental health condition' were used to conditionaly replace the missing values of "Do you believe your productivity is ever affected by a mental health issue?"
with either no if they answered yes to having a mental health condition or not applicable to me if they answered yes.

Data was then loaded into power BI to answer questions from the data including: Has employers handling of mental health improved over time as rated by employees? How many working hours were lost due to poor mental health?
As well as showing demographic differences in mental health between facotrs such as gender, age and location. 
