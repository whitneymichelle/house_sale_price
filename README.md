# Home Sale Price Prediction Model
#### Home sale price predictive model and deployment in R shiny dashboard.

Dataset used was from House Prices: Advanced Regression Techniques Kaggle competition. 
For this project, only the training dataset was used for model building and deployment. 
Here is a link to information on the Kaggle competition: https://www.kaggle.com/c/house-prices-advanced-regression-techniques

## Requirements

### Libraries
- shiny
-	shinyWidgets
-	DT
-	scales
-	grid
-	gridExtra
-	tidyverse
-	skimr
-	janitor
-	tidymodels
-	vip
-	xgboost
-	openxlsx


### From the Repository

Download content of the repository. Run `shiny_dashboard/model_app_main` to deploy model predictions within the shiny app, changing **setwd()** to your desired local directory where you have saved repository files.

This file sources needed to run the shiny app and sourced within `shiny_dashboard/model_app_main` are:

**Final Model Script**
- `House Prices Predictive Model/model_main.R`

In this script, the data is imported, preprocessed, and the model fitted using tidymodels package. The fitted model parameters and hyperparameters were finalized in this script after several model iterations, and predictors were pared down to top 10 most important variables. To see visual representation of top 10 most important variables' influence on the model, open `House Prices Predictive Model/model_output_files/imp_var_plot.png`. Description of all data variables, including those inputted in the model before model was finalized, are here: `House Prices Predictive Model/data_description.txt`.

**Shiny UI and Server**
- `House Prices Predictive Model/course_dashboard/model_app_ui.R`
- `House Prices Predictive Model/course_dashboard/model_app_server.R`

The server takes in user inputs, the model's predictors, and the model is used to predict the house sale price.

## R Session Information

- Session info -------------------------------------------------------------------------------------------------------------------
 setting  value                       
 version  R version 3.6.1 (2019-07-05)
 os       Windows >= 8 x64            
 system   x86_64, mingw32             
 ui       RStudio                     
 language (EN)                        
 collate  English_United States.1252  
 ctype    English_United States.1252  
 tz       America/Chicago             
 date     2020-11-08                  

- Packages -----------------------------------------------------------------------------------------------------------------------
 package     * version date       lib source        
 assertthat    0.2.1   2019-03-21 [1] CRAN (R 3.6.3)
 cli           2.0.2   2020-02-28 [1] CRAN (R 3.6.3)
 crayon        1.3.4   2017-09-16 [1] CRAN (R 3.6.3)
 digest        0.6.25  2020-02-23 [1] CRAN (R 3.6.3)
 fansi         0.4.1   2020-01-08 [1] CRAN (R 3.6.3)
 fastmap       1.0.1   2019-10-08 [1] CRAN (R 3.6.3)
 glue          1.4.2   2020-08-27 [1] CRAN (R 3.6.3)
 htmltools     0.5.0   2020-06-16 [1] CRAN (R 3.6.3)
 httpuv        1.5.4   2020-06-06 [1] CRAN (R 3.6.3)
 later         1.1.0.1 2020-06-05 [1] CRAN (R 3.6.3)
 magrittr      1.5     2014-11-22 [1] CRAN (R 3.6.3)
 mime          0.9     2020-02-04 [1] CRAN (R 3.6.2)
 promises      1.1.1   2020-06-09 [1] CRAN (R 3.6.3)
 R6            2.4.1   2019-11-12 [1] CRAN (R 3.6.3)
 Rcpp          1.0.5   2020-07-06 [1] CRAN (R 3.6.3)
 rlang         0.4.7   2020-07-09 [1] CRAN (R 3.6.3)
 rstudioapi    0.11    2020-02-07 [1] CRAN (R 3.6.3)
 sessioninfo * 1.1.1   2018-11-05 [1] CRAN (R 3.6.3)
 shiny         1.5.0   2020-06-23 [1] CRAN (R 3.6.3)
 withr         2.2.0   2020-04-20 [1] CRAN (R 3.6.3)
 xtable        1.8-4   2019-04-21 [1] CRAN (R 3.6.3)
 yaml          2.2.1   2020-02-01 [1] CRAN (R 3.6.3)

