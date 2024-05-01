# Framingham-

I. Provide some brief background to your project and the scientific question that you are going to answer;

Our aim is to investigate possible indicators to higher blood pressure, a health indicator of poor heart function.  

Scientific Questions: 

 Determine the following continuous variables: cigarettes smoked/day, heart rate, glucose level, total cholesterol, and BMI, and their effect on blood pressure.

Determine the following discrete variables:  sex, education, smoking status, diabetes status, and their effect on blood pressure.

Is there any interaction between these variables that contribute to a better fitting model? 

Model building method:  We will start with a forward selection strategy, starting with single explanatory variables, and adding other variables and interactions to see if they add value to a better model.  

II
. Briefly summarize the dataset you have selected, making sure that you provide the source of the dataset (e.g., provide the web address) and information about the variables.

Data source: https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset/data
Code: https://amyylin1.github.io/Framingham-/

This Framingham heart study is a longitudinal study that tracks N = 4,240 individuals aged between 32 to 70 years old in Framingham, Massachusetts. The dataset consists of 15 explanatory variables and its prevalence on heart disease. The explanatory variables are used to investigate lifestyle/habits and environmental factors that may influence the event of cardiovascular diseases such as myocardial infarction, hypertension, stroke, congestive heart disease, etc. in men (n = 2,420) and women (n = 1,820). The Framingham data helps many scientists, statisticians, physicians, and other health care workers understand the risk/development  and prediction of heart disease in the next 10 years based on the variables.

Response variable: 

Blood pressure is a standard health measure of cardiovascular function.  In general, higher blood pressure indicates poor vascular health, and lower blood pressure suggests otherwise.  Therefore, we decide to make our response variable, the difference between the systolic blood pressure and the diastolic blood pressure.

 “sysBP” - Systolic Blood Pressure of an individual measured in mmHg
 “diaBP” - Diastolic Blood Pressure of an individual measured in mmHg

Y = Difference bet. sysBP and diaBP =  sysBP - diaBP

In addition, we will perform a logarithmic transformation of Y(sysBP - diaBP) to normalize skewed data. 

Explanatory Variables at intake examination of participants:

B1: ”male” - indicating factor for gender where 1= female and 0 otherwise (male) 
B2: “age” - age in years of participant 
B3: “education” - indicating factor for the level of education where 1= some highschool, 2= high school/GED, 3= some college, 4= college and 0 otherwise (N/A) 
B4: “currentSmoker” - indicating factor for smoking status where 1= yes and 0 otherwise (no) 
B5: “cigPerDay” - The average amount of cigarettes smoked per day 
B6: “BPMeds” - indicating factor for current status of taking blood pressure medication where 1= yes and 0 otherwise (no) 
B7: “prevalentStroke” - indicating factor for the prevalence of stroke where 1= yes and 0 otherwise (no)
B8: “prevalentHyp” - indicating factor for the prevalence of hypertension where 1= yes and 0 otherwise (no)
B9: “diabetes” - indicating factor for prevalence of diabetes where 1= yes and 0 otherwise (no)
B10: “totChol” - Total cholesterol serum level of an individual measured in mg/dL
B13: “BMI” - Body Mass Index of an individual measured in (weight) kg/m2 (height)
B14: “heartRate” - Heart rate (ventricular rate) measured in beats/minute
B15: “glucose” - Glucose serum in blood measured in mg/dL
“TenYearCHD” - indicating factor for whether the individual will develop heart disease in the next 10 years from intake examination where 1= yes and 0 otherwise (no)
