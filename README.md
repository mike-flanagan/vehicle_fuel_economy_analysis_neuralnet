![image](https://github.com/mike-flanagan/vehicle_fuel_economy_analysis_neuralnet/blob/main/images/readme_header.jpg?raw=true)
  
<div align="center";>Photo by <a href="https://unsplash.com/@ftm3000?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Tommy Krombacher</a> on <a href="https://unsplash.com/s/photos/fuel?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></div>  
  
## Overview  
This project develops a predictive model for the MPG or MPGe of a vehicle based on various qualities that a vehicle may have.  
  
## Motivation  
President Biden has unveiled a new target that calls for U.S. emissions to be 50-52% lower in 2030 than they were in 2005. According to the EPA, U.S. emissions were only about 13% below 2005 levels, which suggests that much more than what has been done in the past 15 years will need to be done to reach the stated target within the next 10 years. With such a bold goal coming from the U.S. administration, there are likely to be new regulatory measures taken to fascilitate energy efficiency in the automotive industry. I aim to develop a predictive model that may help auto manufacturers better navigate upcoming regulations by informing them of what qualities may have the largest impact on MPG/MPGe.
  
## Data  
The dataset is sourced from the EPA's [fueleconomy.gov](https://fueleconomy.gov/) and includes roughly 43,500 items, with each row representing a unique vehicle of various makes, models, and years since 1984. It comes with 83 features representing a thorough set of qualities that a vehicle may have. The target variable `y` represents the combines city/highway MPG for internal combustion engine (ICE) vehicles, or the combined city/highway MPGe (miles per gallon equivalent) for plug-in hybrid electric vehicles (PHEVs) and pure battery powered vehicles (BEVs). 
  
## Methods  
My methodology implements the CRISP-DM model for exploratory data analysis, cleaning, modeling, and evaluation. I use descriptive and inferrential statistics to evaluate the dataset, implemented an extensive cleaning process to fascilitate improvements to my model and allow for ease of data management. My models use regression analysis to identify which features of a vehicle best inform its predictions. Using `keras`' RandomizedSearchCV() and `scikitlearn`'s wrapper method, I was able to run over 100 **neural networks** for regression and identify which performed best, and compare the results with a simple linear regression model. Models were evaluated primarily on the Mean Square Error of training, validation and testing data in a train-test-split.  
  
Tools used include Python, Keras, TensorFlow, SciKit Learn, NumPy, Pandas, and SciPy. Visualizations were created with MatPlotLib and Seaborn.  
  
## Conclusion  
After running and evaluating different models, I selected the model which returned the lowest MSE on the validation data, which scored an MSE of 4.01 (RMSE of 2). The model was then fit to the full training dataset to generate prediction on the target, and scored on the testing dataset with an MSE score of 19.6 (RMSE of 4.3). For context, the standard deviation for the target MPG/MPGe of all vehicles is 8.7, and 5.3 for the dominant class of gas-powered internal combustion engine vehicles.  
  
## Further Actions  
I would like to continue my CRISP-DM process by returning to the dataset and making use of features that were set aside for my first attempts at modeling. As internal combustion engine vehicles were substantially the dominant class, I'm curious if developing a model only for internal combustion engine vehicles would output for predictions. Also, in line with my motivation for the project, I would like to restart the process using an alternative feature for a target: the included $CO_2$ emissions and other pollutants. There is no one correct approach to evaluating and using the data, but to go further, it would be useful to improve my domain expertise in automobiles and mechanical engineers, develop a deeper familiarity with regulatory policy for automotives/the energy sector, and utilize the insights of others who may have a different creative approach. There are even more features that I can imagine would help my model, so I am also interested in supplementing my data with exogenous variables, such as vehicle weight and other vehicle traits not included in the EPA's dataset. In the final notebook, I have outlined other thoughts on how the model could be improved with more ideas on cleaning and feature engineering.  
  
## Index
- **data/** — contains vehicles dataset used throughout project.   
- **EDA/** — contains initial project development/data exploration file, initial EDA notebook file, and initial modeling notebook file. 
- **images/**  — contains a PDF presentation of my findings, images files used for notebook and readme header, and output visualizations which were used in the presentation slides.
- **MPG_NeuralNet_Final_Notebook.ipynb** — primary project notebook  
- **README.md**  
  
  
  
<div align="center";>Author  
  <div align="center";>Mike Flanagan  
    
[GitHub](https://github.com/mike-flanagan/) | [LinkedIn](https://www.linkedin.com/in/mike-flanagan-data/)
  
  
