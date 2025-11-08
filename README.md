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

2. Range: What are the unique values for each categorical column? What is the range of values of the numeric columns? Are the numeric column values normally distributed?
   
   (1) Unique values for each caegorical column:
      DISTRICT_TYPE
      School District         17960
      Legislative District     2702
      All                        43
      Name: count, dtype: int64
   
      DISTRICT_NAME
      Southern Trinity Joint Unified              56
      Trinity County Office of Education          55
      Santa Barbara County Office of Education    54
      Big Sur Unified                             50
      Spencer Valley Elementary                   50
                                                  ..
      West Contra Costa Unified                   16
      Oroville Union High                         15
      Visalia Unified                             15
      Fairfield-Suisun Unified                    13
      San Francisco Unified                       13
      Name: count, Length: 692, dtype: int64

      ACADEMIC_YEAR
      2018-2019    20705
      Name: count, dtype: int64

      DEMO_CATEGORY
      Race               12116
      Foster Status       2754
      Homeless Status     2308
      Gender              2291
      All                 1236
      Name: count, dtype: int64

      STUDENT_POPULATION
      None Reported                                1927
      American Indian or Alaska Native             1833
      Native Hawaiian or Other Pacific Islander    1810
      Foster Youth                                 1739
      Two or More Races                            1539
      Black or African American                    1484
      Experienced Homelessness in K-12             1472
      Asian                                        1372
      All                                          1236
      Male                                         1171
      Female                                       1120
      White                                        1089
      Hispanic or Latino                           1062
      Not Foster Youth                             1015
      Did Not Experience Homelessness in K-12       836
      Name: count, dtype: int64





   (2) Range of values of the numeric columns:

   

