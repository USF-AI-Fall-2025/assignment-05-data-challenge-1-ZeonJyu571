# x62-data-challenge-student-pathways

1. Data quality: For each feature (column), what is the data type? Is there any missing data?

   Please refer to the follwing sheet for data type of each column. There are 2745 entries of DISTRICT_CODE missing.
   
  <class 'pandas.core.frame.DataFrame'>
  RangeIndex: 20705 entries, 0 to 20704
  Data columns (total 11 columns):
   #   Column              Non-Null Count  Dtype  
  ---  ------              --------------  -----  
   0   DISTRICT_TYPE       20705 non-null  object 
   1   DISTRICT_NAME       20705 non-null  object 
   2   DISTRICT_CODE       17960 non-null  float64
   3   ACADEMIC_YEAR       20705 non-null  object 
   4   DEMO_CATEGORY       20705 non-null  object 
   5   STUDENT_POPULATION  20705 non-null  object 
   6   AWARD_CATEGORY      20705 non-null  object 
   7   WAGE_YEAR1          20705 non-null  float64
   8   WAGE_YEAR2          20705 non-null  float64
   9   WAGE_YEAR3          20705 non-null  float64
   10  WAGE_YEAR4          20705 non-null  float64
  dtypes: float64(5), object(6)
  memory usage: 1.7+ MB

2. Range: What are the unique values for each categorical column? What is the range of values of the numeric columns? Are the numeric column    values normally distributed?
   
   (1) Unique values for each caegorical column:
   
      DISTRICT_TYPE
array(['School District', 'Legislative District', 'All'], dtype=object)
   
      DISTRICT_NAME
   There are 692 unique values, below are 6 examples of them:
array(['Duarte Unified', 'Coronado Unified', 'Gilroy Unified',
      ......
       'Fontana Unified', 'Assembly District 5', 'Redlands Unified'],
      dtype=object)

      DISTRICT_CODE
   There are 571 unique values, below are 6 examples of them:
   array([1964469., 3768031., 4369484., 5672553.,
         ......
          3667710., 3667843.])
   

      ACADEMIC_YEAR
array(['2018-2019'], dtype=object)

      DEMO_CATEGORY
array(['Race', 'Homeless Status', 'All', 'Foster Status', 'Gender'],
      dtype=object)

      STUDENT_POPULATION:
   array(['None Reported', 'Black or African American',
       'Did Not Experience Homelessness in K-12',
       'American Indian or Alaska Native',
       'Native Hawaiian or Other Pacific Islander', 'All',
       'Two or More Races', 'Foster Youth', 'Female', 'White',
       'Experienced Homelessness in K-12', 'Not Foster Youth', 'Male',
       'Asian', 'Hispanic or Latino'], dtype=object)

      AWARD_CATEGORY:
array(["Bachelor's Degree - Did Not Transfer", 'Associate Degree',
       'Community College Certificate', "Bachelor's Degree - Transferred"],
      dtype=object)

   (2) Range of values of the numeric columns and whether they are normally distributed:
   
      WAGE_YEAR1: range of values is 97993, not normally distributed.
      WAGE_YEAR2: range of values is 132847, not normally distributed.
      WAGE_YEAR3: range of values is 146728, not normally distributed.
      WAGE_YEAR4: range of values is 153910, not normally distributed.
   
      <img width="592" height="207" alt="image" src="https://github.com/user-attachments/assets/4feb880d-83e4-4d3f-b31c-310a6e421f07" />
      <img width="602" height="443" alt="image" src="https://github.com/user-attachments/assets/4b89c0b2-2952-4a85-ad05-e51c0f88db92" />


4. Semantics: What is the meaning of the columns? Are any columns related to other columns? (If so, how?)

   The variables DISTRICT_TYPE, DISTRICT_NAME, DISTRICT_CODE, ACADEMIC_YEAR, and WAGE_YEAR simply mean what their names suggest. The variable of DEMO_CATEGORY is a list of demographic variables, its value means which demographic variable is used to measure the student, and STUDENT_POPULATION shows the corresponding value of the demographic variable in question. AWARD_CATEGORY presents the degree the student achieved, however, for bachelor's degree, it provided extra information on whether they were transferred student.

   DISTRICT_CODE maps to DISTRICT_NAME:
   <img width="563" height="108" alt="image" src="https://github.com/user-attachments/assets/89ac8102-4d18-444c-9440-c10cf1ec3b37" />

   The wages of all four years are positively correlated to each other:
   <img width="649" height="157" alt="image" src="https://github.com/user-attachments/assets/45861cfc-63db-41f0-83c0-ccd41d079b64" />

4.1 Which demographic shows the highest WAGE_YEAR3? Which demographic shows the lowest WAGE_YEAR3? 

      <img width="607" height="558" alt="image" src="https://github.com/user-attachments/assets/c82d2cf9-80f8-43e9-898c-5b90115b0bb2" />

      For foster status, "Not Foster Youth" has the highest WAGE_YEAR3, "Foster Youth" the lowest;
      For Gender, "Male" has the highest WAGE_YEAR3, "Female" the lowest;
      For Homeless Status, "Did Not Experience Homelessness in K-12" has the highest WAGE_YEAR3, "Experienced Homelessness in K-12" the lowest;
      For Race, "White" has the highest WAGE_YEAR3, "None Reported" the lowest.

4.2 & 4.3 Are there any people with negative/positive wage trends? Describe these people by their demographics.

      Every group demonstrates a positive wage trend.

      <img width="727" height="677" alt="image" src="https://github.com/user-attachments/assets/aecdf046-ae03-4e63-8c2f-c880607ac2a4" />


      

   

