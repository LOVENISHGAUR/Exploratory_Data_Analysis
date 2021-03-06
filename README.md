# Author : Lovenish

# Exploratory_Data_Analysis

Layman Idea

Imagine you and your friends decides to meet over the weekend cause it's been too long and decide to do some activity.There is absolutely no debate about that,it will lead to a state where you find yourself puzzled with lot of questions which needs to be answered in order to make a decision.Being a good chieftain the first question you would ask, where we should go?As a regular practice,you would also brouse various applications and google to get theidea.Furthermore,you’d find out activity you can perform and then what are the ratings of the places you selected to do the activity may it be movie, dinner, clubbing or some adventure sports.
Whatever investigating measures you would take before finally buying tickect for your clan ,is nothing but what data scientists in their lingo call ‘Exploratory Data Analysis’.


"""
Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations.
"""

EDA explained using sample Data set:
To share my understanding of the concept and techniques I know,I’ll take an example of white variant of Wine Quality data set which is available on UCI Machine Learning Repository and try to catch hold of as many insights from the data set using EDA.

#Machine learning

#******************************************************************************
# TYPES OF PREDICTIVE MODELS

 1. SUPERVISED LEARNING : We have the target variable 
 
 1.1 REGRESSION : where the target variable have continuous values
 
 1.2 CLASSIFICATION : Where the targeT variable have the discrete value (i.e 0 or 1, yes or no)

 2. UNSUPERVISED LEARNING : we do not have the target variable 
 
  2.1 CLUSTURING
  
   2.1.1 DOCUMENT CLUSTURING
   
   2.1.2 SEGMNENTATION


#******************************************************************************
# STAGES OF PREDICTIVE MOFDELLING

# We can broadly divide the model building life cycle in six stages

 1. PROBLEM DEFINANTION
 
 2. HYPOTHESIS GENERATION : LISTING DOWN ALL THE POSSIBLE VARIABLES, WHIXH MIGHT INFLUENCE THE PROBLEM OBJECTIVE
 
 3. DATA EXTRACTION/ COLLECTION : 
 
 4. DATA EXPLORATION AND TRANSFORMATION
 
   4.1 Reading the data
   
   4.2 Variable identification
   
       4.2.1 To identify VARIABLES
       
        4.2.1.A) INDEPENDENT : THESE HELPIN PREDICTING THE DEPENDENT VARIABLE
        
        4.2.1.B) DEPENDENT : THE VARIABLE WE ARE TRYING TO PREDICT
        
       4.2.2 To IDENTIFY VARIABLEs
       
        4.2.2.A) CONTINUOUS
        
        4.2.2.B) DISCRETE/CATEGORICAL
        
   4.3 Unvariate analysis : EXPLORE ONE VARIABLE AT A TIME,  SUMMARIZE THE VARIABLE,  MAKE SENSE OUT OF THAT SUMMARY TO DISCOVER INSIGHTS AND ANNOMALIES.
   
       4.3.1 FOR CONTINUOUS VARIABLES
       
        4.3.1.A) TABULR METHOD : MEAN, MEDIAN, STANDARD DEVIATION AND MISSING VALUES
        
        4.3.1.B) GRAPHICAL METHOD : DISTRIBUTION OF VARIABLES AND OTLIERS DETECTION
        
       4.3.2 FOR CATEGORICAL VARIABLES : COUNT AND COUNT%
       
        4.3.2.A) TABULR METHOD : FREQUENCY TABLE
        
        4.3.2.B) GRAPHICAL METHOD : BAR PLOT
        
   4.4 Bivariate analysis : TO SEE IF TWO VARIABLES ARE ASSOCIATED WITH EACH OTHER OR NOT 
   
       4.4.1 FOR CONTINUOUS VARIABLES
       
        4.4.1.A) BOTH VARIABLES ARE CONTINUOUS : SCATTER PLOT
        
        4.4.1.B) ONE VARIABLE IS CONTINUOUS ND OTHER ONE IS CATEGORICAL : BAR PLOT : TWO SAMPLE t-Test
        
        4.4.1.C) BOTH CATEGORICAL VARIABLE : TWO WAY TABLE , CHI-SQUARE TEST
        
   4.5 Missing value treatment
   
       4.5.1 MISSING COMPLETELY AT RANDOM (MCAR) : THE MISSING VAULE HAVE NO RELATION TO THE VARIABLE FOR MISSING VALUE EXIST AND OTHER VARIABLES IN DATASET.
       
       4.5.2 MISSING AT RANDOM (MAR) : HAVE NO RELATION tO THE VARIABLE FOR WHICH MISSING VALUE EXIST BUT HAVE THE RELATION WITH OTHER VARIABLES IN THE DATASET.
       
       4.5.3 MISSING NOT AT RANDOM (MNAR) : HAVE RELATION TO THE VARIABLE FOR WHICH MISSING VAULE EXIST
       
   4.6 Outlier treatment
   
   4.7 Variable transformation
   
       4.7.1 TAKING LOG OF THE VARIABLES : REDUCE RIGHT SKEWEDNESS
       
       4.7.2 TAKING SQUARE ROOT OF THE VARIABLES : USED FOR RIGHT SKEWED VARIABLES WITH POSITIVE VAULES ONLY
       
       4.7.3 TAKING CUBE ROOT OF THE VARIABLES :  USED FOR RIGHT SKEWED VARIABLES WITH POSITIVE AND NEGATIVE VAULES ONLY
       
       4.7.3 BINNING : USED FOR CONVERTING CONTINUOUS VARIABLES INTO CATEGORICAL VARIABLES.
       
 5. PREDICTIE MODELLING
 
 6. MODEL DEPLOYMENT AND IMPLEMENTATION

#******************************************************************************

# EVALUATION METRICES

 1. CONFUSION MATRIX : A confusion matrix is a table that is often used to describe the performance of a classification model (or “classifier”) on a set of test data for which the true values are known. It allows the visualization of the performance of an algorithm.



 2. ACCURACY : (TRUE POSITIVES(TP) + TRUE NEGATIVE(TN))/(FALSE POSITIVES(FP)+ FALSE NEGATIVE(FN)+TRUE POSITIVES(TP) + TRUE NEGATIVE(TN))
 
   2.1 ALTERNATIVES OF ACCURACY 
   
       2.1.1 TRUE POSITIVE RATE : TP/(TP+FN)
       
       2.1.1 FALSE NEGATIVE RATE : FN/(TP+FN)
       
       2.1.1 FALSE POSITIVE RATE : FP/(FP+TN)
       
       2.1.1 TRUE NEGATIVE RATE : TN/(FP+TN)
       

 3. PRECISION AND RECALL
 
   3.1 PRECISION : OUT OF ALL POSITIVE PREDICTON HOW MANY ARE ACTUALLY POSITIVE.THAT IS 
                   PRECISION =  TP/(TP+FP)
                   
   3.2 RECALL : #   3.1 PRECISION : OUT OF ALL THE ACTUAL POSITIVE, HOW MANY HAVE BEEN PREDICTED AS POSITIVE.THAT IS 
                   RECALL = TP/(TP+FN)
                   
   3.3 F1 SCORE = 2/((1/PRECISION)+(1/RECALL))
   

 4. THRESHLODING : USED IN CASE OF PROBABLITIES IS GIVEN FOR ALL THE OBSERVATION AND THEN WE DEFINE THE THRESHOLD PROBABLITY AND ASSIGN VAULES ACCORDINGLY TO ALL THE OBSERVATION.
 

 5. AUC-ROC : IT IS PLOTTED BETWEEN TPR AND FPR, 
 
       AUC : AREA UNDER THE CURVE
       
       ROC : RECEIEVER OPERATING CHARACTERISTIC : IT IS THE EVALUATION METRIC FOR BINARY CLASSIFICATION
       
   NOTE : AUC-ROC : IT CANNOT BE USED FOR COMPARING TWO MODELS

 6. LOG LOSS : USED FOR COMPARING TWO MODELS 

 7. EVALUATION METRICS FOR REGRESSION PROBLEMS
 
       ERROR = PREDICTED - ACTUAL
       
   7.1 MEAN ABSOLUTE ERROR
   
   7.2 MEAN SQUARE ERROR : PROBLEM WITH THIS IS THAT IT CHANGES THE UNIT OF MEASUREMENT
   
   7.3 ROOT MEAN SQUARE ERROR : 
   
   7.4 ROOT MEAN SQUARE LOG ERROR
   
   7.5 R SQUARE : PROBLEM WITH R SQUARE IS THAT WHEN WE ADD ORE FEATURES THE VAULE EITHER INCREASES OR REMAINS THE SAME IT NEVER DECREASES
   
   7.6 ADJUSTED R-SQUARE
   

#******************************************************************************

