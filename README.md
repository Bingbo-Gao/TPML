# TPML
The method puts forward a new way to integrate the spatial autocorrelation law and property similarity principle into one in a unified machine learning method. 
The TPML model includes the following six steps:

(1) Calculate the difference in paired observations, including the difference in SHM concentration and corresponding difference in covariates;

(2) Build a machine learning model using the difference in SHM concentration as the response variable and the corresponding difference in covariates as predictors;

(3) Predict the SHM concentration difference between observed and unobserved points;

(4) Determine how many neighbors should be included in the final prediction through the cross-validation method based on the predicted concentration difference;

(5) Obtain near observations to attend the final prediction for each unobserved point;

(6) Predict the concentrations at the unobserved points and estimate the uncertainty using selected near observations.


The model validation experiment includes following five steps：

（1）Prepare data and extract the values of the covariates at all points.

（2）Draw samples with the size as 50, 100, 150, 200, 250, 300, 350, 400, 450, 500, 550 and 600 from the points with Mean of the Shortest Distances (MMSD) and Spatial Simulated Annealing (SSA).
Treat the points in each sample as an training data, and corresponding unselected points as validation data. Every row of the training data and data validation include one target  variable value and its covariates values. 
As in practice of spatial sampling, the spatially even coverage is most concerned. The training data of the cross validation here simulated the realistic spatial sampling with different sample size.

（3）Build TPML model, LRK, RF, RFRK and fit the variograms with each training data set separately. 

（4）Predict the target  variable values at validation points using the TPML, OK, LRK, RF and RFRK.

（5）Compare the validation results of these methods.
