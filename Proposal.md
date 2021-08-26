
# flight_delay_prediction
UofA Data Analytics Bootcamp Final Group Project

**Team**:  
* Nicole Lund: <a href="https://www.linkedin.com/in/nicolelund-1/" target="_blank">https://www.linkedin.com/in/nicolelund-1/</a>
* Amber Royster: <a href="https://www.linkedin.com/in/amber-royster/" target="_blank">https://www.linkedin.com/in/amber-royster/</a>
* Anne Niemiec: <a href="https://www.linkedin.com/in/anne-niemiec/" target="_blank">https://www.linkedin.com/in/anne-niemiec/</a>
* Tarak Patel: <a href="https://www.linkedin.com/in/tarakpatel-1/" target="_blank">https://www.linkedin.com/in/tarakpatel-1/</a>

## Problem
Employees with frequent business travel experience time lost with family and productive work time while in transit. In order to minimize lost time, past flight history will be examined and modeled to predict which flight routes experience the smallest delay times.

## Source Data
The Kaggle dataset provides flight performance data for each year between 2009 and 2018. The full data set requires 7.1 Gb of storage space. <a href="https://www.kaggle.com/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018" target="_blank">https://www.kaggle.com/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018</a>

airport_codes.csv provides a lookup table of airport codes to city name. <a href="https://www.transportation.gov/policy/aviation-policy/airport-codes-txt" target="_blank">https://www.transportation.gov/policy/aviation-policy/airport-codes-txt</a>

Airport codes and lat/lng coordinates. <a href="https://datahub.io/core/airport-codes#resource-airport-codes" target="_blank">https://datahub.io/core/airport-codes#resource-airport-codes</a>

## Resource and Scope Management
In order to manage project scope and operate within the constraints of the available tools, the 2017 data will be used to train and test machine learning models and the 2018 data will be used to create flight delay time predictions for visualizations.  The data will be further restricted to only model and predict flight delay times for flights departing from Tucson International Airport (TUS).

## Machine Learning Requirements
Prior to developing machine learning models, the data features will be analyzed to understand any existing correlations. Several machine learning models will be deployed and tuned with uncorrelated features of interest.  Acceptable models will yield accuracy > 0.7, but the model with highest accuracy will be chosen as the model of best fit. 

## Initial Task Assignments
* **Nicole:** Github repository management
* **Tarak:** AWS bucket management
    * Input files downloaded from Kaggle
        * 2017.csv
        * 2018.csv
    * Output files from Data Wrangling
        * 2017_TUS.csv
        * 2018_TUS.csv
* **Tarak:** Data Wrangling
    * Tools: Jupyter Notebook(s), Python, Pandas
    * Initial wrangling:
        * Filter down to flights originating at TUS
        * Add feature column containing the flight's day of the week
* **Nicole:** Feature Assessment
    * Tools: Jupyter Notebook or Google colab
    * Disentangle correlated feature columns from the data
        * Logical assessment
        * Cross-correlation matrix assessment
* **Nicole:** Machine Learning
    * Tools: Google Colab, Pyspark
    * Model flight delay time
* **Everyone:** Visualization
    * Tools: Tableau
    * **Tarak:** Investigate if Tableau public can retrieve data directly from AWS with a connector
* **Amber:** Host application on Github pages
    * Tools: HTML
    * Embed tableau dashboard(s) into a webpage(s)
    * <a href="https://san-wang.github.io/blog/Embed-Tableau-dashboard-into-github-page-post/" target="_blank">https://san-wang.github.io/blog/Embed-Tableau-dashboard-into-github-page-post/</a>
    
## Initial Repository File Structure
* assignment_instructions: Assignment description document
* data_manipulation_modeling:
    * data__raw: Raw data files < 100mb in size
    * data_clean: 
        * Jupyter notebooks for cleaning the data 
        * Clean csv files < 100mb. If a csv needs to be stored in your local repo prior to uploading to AWS, you can save it here and then add the file to .gitignore.
    * feature_assessment: Jupyter notebooks for analyzing cross-correlation of features in the data set.
    * investigate_models: Google colab notebooks for multiple model types
    * model_best_fit: Final Google colab model notebook
* image: Any screen captures or webpage images
* static: Webpage source files
* index.html: Landing webpage
* LICENSE: MIT Standard License
* Proposal.md: Proposal Document
* README.md: Github Repository README