# Time-Series-Project-Simonas
Project README: Macroeconomic Drivers of GDP Growth

This project empirically examines the factors influencing GDP growth, with a specific focus on fiscal policy. Using a Structural Vector Error Correction Model (SVECM), the study analyzes quarterly FRED data from 1984 to 2020 to determine the impact of labor productivity, investment, consumption, unemployment, and interest rates on the economy.
Project Structure

The repository is organized into three main directories:
1. Data

Contains the raw and processed datasets used for the analysis.

    GDP_inference.csv: The primary dataset imported from FRED.

    GDP_inference_clean.csv: The final dataset used for modeling after preprocessing and transformations.

2. Notebooks

Jupyter notebooks used for the iterative research process.

    EDA.ipynb: Exploratory Data Analysis, including time series plotting, Augmented Dickey-Fuller tests for stationarity, and Johansen tests for cointegration.

    Feature_engineering.ipynb: Implementation of log transformations and Cholesky decomposition ordering.

    Models.ipynb: Estimation of the SVECM and generation of Impulse Response Functions (IRF).

3. Src (Source Code)

Modular Python and SQL scripts for data management and model logic.

    Data_utils.py: Utility functions for data handling.

    Feature_engineering.py: Production-ready code for data transformations.

    Models.py: Logic for the SVECM estimation and structural matrix definitions.

    Scraping.py: Scripts used to import data from FRED.

    cleaning_data.sql: SQL scripts for initial data cleaning and handling structural breaks.

Key Methodology

The project utilizes an SVECM because the variables are integrated of order I(1) and exhibit cointegration. The structural matrix is identified using Cholesky decomposition with the following economic ordering:

    Labor Productivity 

    Government Spending 

    GDP 

    Consumption 

    Investment 

    Unemployment Rate 

    Inflation 

    Federal Funds Rate 

Summary of Results

    Primary Drivers: Consumption (+1.0%) and investment (+0.7%) are the most significant drivers of GDP growth.

    Negative Impact: Unemployment significantly lowers GDP growth, consistent with Okun's Law.

    Fiscal Policy: Government spending increases GDP by approximately 0.5% in the long run, suggesting a fiscal multiplier of less than 1.

    Insignificant Factors: Labor productivity and inflation showed statistically insignificant effects in this specific empirical model.