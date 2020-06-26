# diamond-price-prediction

## Objective
To build a web application where users can look up a predicted price for their desired diamonds.  
## Data
For this project, I used a dataset from pycaret’s dataset folder on GitHub, performed data preprocessing transformations, and built a regression model to predict the price ($326-$18,823) of the diamond using basic diamond measurement metrics. Each diamond in this dataset is given a price. The price of the diamond is determined by 7 input variables:  
Carat Weight: 0.2Kg - 5.01Kg  
Cut: Fair, Good, Very Good, Premium, Ideal  
Color: from J (Worst) to D (Best)  
Clarity: I1 (Worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (Best)  
Polish: ID (Ideal), EX (Excellent), G (Good), VG (Very Good)  
Symmetry: ID (Ideal), EX (Excellent), G (Good), VG (Very Good)  
Report: AGSL (American Gem Society Laboratories), GIA (Gemological Institute of America)  

## Tasks
Model Training and Validation: Train, validate models, and develop a machine learning pipeline for deployment using Python (PyCaret).  
Front End Web Application: Build a basic HTML front-end with an input form for independent variables (Carat Weight, Cut, Color, Clarity, Polish, Symmetry, Report).  
Back End Web Application: Using a Flask Framework.  
Deployment of the web application: Using Heroku, once deployed, it will become publicly available and can be accessed via a Web URL.  
## Project Workflow

Machine Learning Workflow (from Training to Deployment on PaaS)
# Task 1 — Model Training and Validation
Model Training and Validation is carried out in Python (Jupyter Notebooks) using PyCaret to develop a machine learning pipeline and train a regression model. I used the default preprocessing settings in PyCaret.  
This transformed the dataset and came down to 65 features for training as compared to only 8 features in the original dataset.  
Model training and validation in PyCaret:  
Here the Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) have been significantly impacted.  
Residual plot of the Linear Regression Model  
After building the model, I saved it as a file that can be transferred to and consumed by other applications:  
Saving the model creates the entire transformation pipeline based on the configuration defined in the setup() function, inter-dependencies are taken care of too. The whole machine learning pipeline and the linear regression model is now saved in the save_model() function.  
# Task 2 — Front End Web Application
## CSS Style Sheet
CSS (Cascading Style Sheets) describes the presentation of a document written in HTML. It holds information such as color, font size, margins, etc. It is saved as a .css file that links to the HTML code.  

## HTML
For front-end web application I used a simple HTML template and a CSS style sheet for designing the input form. Here’s the HTML code snippet of the front-end page of our web application.  

# Task 3— Back End Web Application
I used the Flask framework to build the back-end web application. Here is the Flask code snippet for the back-end application.  

# Task 4— Deployment of the Web Application
After training the model, building a machine learning pipeline, I deployed the web application on Heroku. I linked a GitHub repository to Heroku. The code for this project can be found on my GitHub repository here.  
