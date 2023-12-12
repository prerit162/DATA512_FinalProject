# DATA512 Final Project

# Impact Analysis of Smoke Fires on Public Health and Safety


# Motivation 

The number of wildfires has been on the rise over the last few years and can have a huge impact on several aspects of a city. The number of fires have increased over the last few years and have a significant impact on the environment. Urban and rural landscapes are impacted in many ways. Urban landscapes suffer a more significant impact due to the density of people living in the city which affects both the quality of human lives and overall infrastructure. Beyond the impact of fires on an immediate level, they also have long term consequences on healthcare, environment, and economic aspects of a city. People living in the city may see an increase in respiratory issues, cardiovascular issues, and road accidents due to low visibility. Apart from their effect on health, fires also have repercussions on the economic conditions through property damage, disruption of businesses, agricultural losses, and tourism. The city council needs to have a proper plan to address all these concerns and make people aware of the measures that they have taken to overcome these losses.  There is also a need to see if a certain group of people are more vulnerable to this and introduce new measures to protect these individuals.

# Aim and Research Questions 

The goal of this submission of the project was to analyze the impact of wildfire on a specific city in the US. The end goal is to be able to inform policy makers, city managers, city councils, or other civic institutions, to make an informed plan for how they could or whether they should make plans to mitigate future impacts from wildfires.

The project was divided into two halves where the first part of the project was focused on the smoke estimate calculation for Derby, Kansas and the second part was extending that analysis to see the impact of fires on Public Health and Safety. In the first part of the project, various techniques were explored such as Linear Regression, ARMA (Autoregressive Moving Average), ARIMA (Autoregressive Integrated Moving Average) models but ended up using SARIMA(Seasonal Autoregressive Integrated Moving Average (SARIMA)) for my forecasting model. This is because SARIMA explicitly incorporates seasonality into the model, which makes it a great fit for the time series data available to us. This helps in utilizing the recurring patterns at regular intervals to make more robust predictions. Also, SARIMA has a more flexible framework which can tune autoregressive and moving average components which allows the model to capture nonlinear patterns present in time series data.

The second phase of the project is the extension plan which focuses on the  impact of these fires on the health and safety of its residents mainly on the following aspects :

●	Respiratory Health Issues : Exposure to wildfire smoke can exacerbate respiratory conditions such as asthma, bronchitis, and chronic obstructive pulmonary disease (COPD)

●	Cardiovascular Effects : Fine particles in smoke can contribute to cardiovascular problems, potentially increasing the risk of heart attacks and other cardiovascular issues.

●	Visibility Reduction : Thick smoke can reduce visibility, posing hazards for drivers and increasing the risk of accidents on roads.

The analysis would revolve around answering the following questions around the impact of smoke fires on residents in Derby, Kansas - 

# Mortality Rates  for Respiratory Diseases, Cardiovascular Diseases and Road Accidents  

●	Possible correlations between increase in smoke fires and mortality rates because of the diseases

●	Which respiratory diseases are shown to have a significant increase  in mortality rates?

●	Observe trends in road accidents at the time of smoke fires due to low visibility.

# Demographic Disparity 

●	Identifying age groups or ethnicities most vulnerable or impacted by health conditions. 

●	Observe change in life expectancy across different demographics.

# Recommendations

The results provide insights into how smoke fires affect various aspects, including respiratory conditions, cardiovascular diseases, and reduced visibility leading to road accidents.

●	The county should implement necessary measures to address the rising mortality rates related to respiratory conditions among females especially for  Chronic obstructive pulmonary disease and Chronic respiratory diseases. This can be done through the following steps  : 

○	Launch targeted health education campaigns to raise awareness about the risks of respiratory conditions, emphasizing the importance of early detection, symptom recognition, and seeking medical attention.

○	Implement regular screening programs, especially for vulnerable populations, to detect respiratory conditions at an early stage. Early detection allows for timely intervention and better management of chronic diseases.

○	Improve access to healthcare services, ensuring that females have easy access to medical facilities, clinics, and specialists for respiratory health check-ups and treatment.

●	 Special attention is required for the AIAN ethnicity group where there has been an increase in mortality rates for respiratory and cardiovascular diseases. Life expectancy has also shown a visible decline for AIAN over the last few years.

○	Understand if the AIAN community is more involved in jobs that are more prone to health issues so that appropriate steps and strategies can be launched to address occupational health disparities.

○	Implement robust programs that can reform and enforce regulations in industries where the AIAN community is employed. Workers need to be educated on potential health hazards and provided with appropriate protective equipment.

○	Improve access to quality education by investing in schools and educational resources within or near AIAN communities. Enhance cultural competence in educational curricula to make them more inclusive.

○	Work with community leaders to act as liaisons between healthcare providers and community members to empower them with healthcare services, including preventive care, screenings, and chronic disease management which can foster trust and cultural understanding.

●	It is advisable to adjust driving guidelines, particularly during periods of increased smoke fires, to ensure road safety.

○	Launch public awareness campaigns to educate people about the risks associated with reduced visibility due to smoke fires. 

○	Utilize emergency alert systems to notify drivers of hazardous conditions caused by smoke fires.

○	Introduce variable speed limits that can be adjusted dynamically based on current visibility conditions.

# Folder Hierarchy

├── <b>Data/</b><br>
&nbsp;&nbsp;&nbsp;├── Smoke_Estimate_Annual.csv<br>
&nbsp;&nbsp;&nbsp;├── aqi_yoy.csv<br>
&nbsp;&nbsp;&nbsp;├── aqi_gaseous.csv<br>
&nbsp;&nbsp;&nbsp;├── aqi_particulate.csv<br>
├── <b>Code/</b><br>
&nbsp;&nbsp;&nbsp;├── Data_Extraction_Analysis.ipynb<br>
&nbsp;&nbsp;&nbsp;├── Reader.py<br>
&nbsp;&nbsp;&nbsp;├── Wildfire_short_sample.json<br>
&nbsp;&nbsp;&nbsp;├── __init__.py<br>
&nbsp;&nbsp;&nbsp;├── test_geocalc.py<br>
├── <b>Output/</b><br>
&nbsp;&nbsp;&nbsp;├── Visualization_1.png<br>
&nbsp;&nbsp;&nbsp;├── Visualization_2.png<br>
&nbsp;&nbsp;&nbsp;├── Visualization_3.png<br>
&nbsp;&nbsp;&nbsp;├── Validation_Forecast.png<br>
&nbsp;&nbsp;&nbsp;├── Test_Forecast.png<br>
&nbsp;&nbsp;&nbsp;├── Test_Forecast_with_CI.png<br>

# Prerequisites
Before using this code, ensure you have the following prerequisites installed:

1.) Python 3

2.) Requests

3.) Pandas

# Data Sources and Description

USGS_Wildland_Fire_Combined_Dataset.json: This contains the Combined wildland fire datasets for the United States and certain territories [Link](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81) 

US City assigned for individual analysis -  [Google spreadsheet](https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit)

The city under consideration for my analysis is Derby, Kansas with coordinates (37.552407, -97.261492)

# Licenses and Reference Code

This project is licensed under the MIT License. The sample codes shared for reference have been provided under the [Creative Commons CC-BY license](https://creativecommons.org/licenses/by/4.0/):

[Sample Code for GeoJSON reader](https://drive.google.com/file/d/1TwCkvdaw0MxJzW7NSDg6XxYQ0dvaS44I/view)

[Sample Code for Distance Computation](https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view)

[Sample Code for fetching data from US EPA Air Quality System API](https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view)


# Reproducibility

The following steps need to followed to run this code seamlessly :

&emsp; Clone this repository to your local machine.<br>

&emsp; Install all the required libraries.<br>

&emsp; Download the jsons - USGS_Wildland_Fire_Combined_Dataset.json and USGS_Wildland_Fire_Merged_Dataset.json from  the following [link](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81) by downloading the GeoJSON Files.zip folder and store these two jsons into the Data Folder<br>

&emsp; Run Data_Extraction_Analysis.ipynb to generate all Visualizations and output csv file stored in Data Folder<br>


# Considerations for Analysis and Reproducibility

&emsp; The input data file needs to be downloaded from the link mentioned under Data Sources and should be kept in the Data Folder for successful Execution of the Python Code<br>

&emsp; The Json Files created in the code are not present under the Data Folder due to its large size and hence need to be stored in the data folder before running the code<br>

&emsp; The distance threshold from the city assigned has been kept at 1250 miles for the time period between 1963 - 2023<br>

&emsp; The data fetched for my city(Derby, Kansas) had data for the time period for the time period between 1963 - 2020 and data was found to be missing post 2020<br>

&emsp; The data is not well distributed and hence fires over the entire year have been considered instead of the fires between 1st May to 31st October.<br>

&emsp; A modified version of ARIMA called SARIMA has been used in forecasting the Smoke Estimate for the next 25 years (2024-2049) along with confidence intervals for thos predictions <br>


# Output

Visualization 1 : Produce a histogram showing the number of fires occurring every 50 mile distance from your assigned city up to the max specified distance.

![image](./Output/Visualization1.png)

Visualization 2 : Produce a time series graph of total acres burned per year for the fires occurring in the specified distance from your city.

![image](./Output/Visualization2.png)

Visualization 3 : Produce a time series graph containing your fire smoke estimate for your city and the AQI estimate for your city.

![image](./Output/Visualization3.png)

Validation Forecast : Created a Validation Set to select the best and optimized parameters for the SARIMA Model

![image](./Output/Validation_Forecast.png)

Test Forecast : Used the Trained Model to make predictions for the 2024 - 2049 period

![image](./Output/Test_Forecast.png)

Test Forecast with CI: Created a plot with Confidence Intervals for the prediction on 2024 - 2049 period

![image](./Output/Test_Forecast_with_CI.png)

# License

This assignment code is released under the MIT License.
