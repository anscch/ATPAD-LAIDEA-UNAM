# ATPAD-LAIDEA-UNAM

ATPAD: An Accessible Tool for RUOA-UNAM Atmospheric Data Processing and Visualization

Several regions of the world are making an effort to meet the atmospheric monitoring needs of each region to generate accurate information for the study of meteorology, 
climate change, and air quality. Monitoring networks generate a large amount of information that needs to be stored, validated, corrected, and interpreted, however, 
practical tools are not always available for the development of these activities without the need to resort to highly trained personnel, thus limiting the way the general population's 
access to atmospheric monitoring information. This work presents a tool for the basic processing and visualization of atmospheric monitoring data, specifically from the 
University Network of Atmospheric Observatories (RUOA) of the National Autonomous University of Mexico. ATPAD (Accessible Tool for Processing Atmospheric RUOA Data) is a project developed in Python 
that allows the manipulation and visualization of pre-processed databases in an easy and freely accessible way.

## DIRECTORIES
To make the user experience easier, we suggest creating the following directories within the working directory. This will allow for an organized management of input and output files without requiring significant modifications to the code.

METEO_RAW: For meteorological input data.

POLLUTION_RAW: For atmospheric pollution input data.

PARQUET_FILES: For pre-processed data in Parquet format.

OUTPUT_FILES: For output files in CSV format.
    
## PREP_ATPAD

The notebook **PREP_ATPAD** takes files from the **METEO_RAW** and **POLLUTION_RAW** directories to merge them into two dataframes: **meteo** and **pollution**. It then formats the column names and generates parquet format files, which will be stored in the **PARQUET_FILES** directory.

## METEO_ATPAD AND POLLUTION_ATPAD

The **METEO_ATPAD** and **POLLUTION_ATPAD** notebooks take input files from **PARQUET_FILES** and apply:  
- Data cleaning and validation  
- Outlier handling  

Cleaned datasets can be filtered by **station** and **time range**.  

Available features:  
- Compute **24-hour averages** (with 75% completeness).  
- Generate **diurnal cycles** (hourly medians).  

Processed datasets can be saved as CSV files in the **OUTPUT_ATPAD** folder.

## VIEW_ATPAD


**VIEW_ATPAD.ipynb** provides **basic visualization tools** for pollution and meteorological datasets previously processed with ATPAD.  

The notebook allows users to:  
- Load cleaned **pollution** and **meteorology** CSV output files.  
- Select and filter data by **time period** and **region**.  
- Generate a variety of exploratory plots, including:
- **Wind roses** and **pollution roses**.
- **Histograms** and **violin plots** for both meteorology and pollution data.  
- **Time series** of pollutants and meteorological parameters across regions.  

## ORIGINAL DATA

https://ruoa.unam.mx/

## License

This project is licensed under the [MIT License (Non-Commercial)](./LICENSE).  
Use of this software is restricted to non-commercial purposes. For commercial use, don't hesitate to get in touch with andres.caschac@gmail.com.
