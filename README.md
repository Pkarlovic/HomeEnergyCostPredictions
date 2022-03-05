## HomeEnergyCostPredictions

Predicting home energy usage using Energy and Weather Data with an LSTM. 

Global Energy Consumption has drastic affects on electrical infrastructure as well as causes negative environmental impacts on local ecosystems. 
The burning of fossil fuels such as coal, oil, and natural gas are one of the largest contributors to Greenhouse Gas Emissions (GHG)
High energy use without proper allotment of energy can yield to environmental and humanitarian disasters such as those witnessed in the 2021 Texas Power Crisis. 

We aim to answer two questions: 

Is it possible to accurately predict for Electrical Energy Consumption at a household level to be able to apply at a regional/local scale?

Is it possible to understand the relationship between energy consumption and climatic variables (weather)?

# Data:

Energy Consumption Data was retrieved from UK Power Networks, which sampled 5,567 London Households which took part in the Low Carbon London Project between November 2011 to February 2014 at 30 minutes intervals.

Weather Data was received from the Meteomatic Weather API which featured standard weather parameters such as temperature, humidity, and visibility. 

# Method: 

For this project, Weather and Consumption data will be imported into Python, where it will be cleaned and analyzed using various libraries. Once formatted, data will be converted into a time series, as well as undergo feature selections to ensure best results for a Long-Term Short Memory Model. 

We plan to use weather variables and Electrical Consumption to predict the amount of electricity consumed in the average household.

# Data Exploration

![image](https://user-images.githubusercontent.com/70538240/156903391-167c1c62-3ccd-4b3e-9af4-49b46bc672bf.png)

We can see that Energy Consumption and Temperature have an inverse relationship indicating as Temperature increases, Consumption Decreases.

![image](https://user-images.githubusercontent.com/70538240/156903415-4a9e088a-f98b-4800-a2bf-d26c45991bd2.png)

The relationship between Consumption and Humidity is correlated indicated that is Humidity Increases so will Energy Consumption

![image](https://user-images.githubusercontent.com/70538240/156903426-0847500a-95ee-4ebb-ac00-b865cac83cf1.png)

The figure shows the relationship between Visibility and Energy Consumption, where as Energy Consumption has an inverse relationship with Visibility.

# What are Long Short-Term Memory Models

LSTM Models are artificial recurrent neural networks capable for tracking and selecting dependencies for new observations using past observations. 

These models excel at making predictions based on time series data as there can be lags of unknown duration between important events in a time series.

# Application into Python

In order to apply the model, we created a weather cluster in order to relate variables such as temperature, visibility and humidity to a weather score (i.e. cluster). The combination of these variables resulted in a score that was used to determine the type of weather at the time of energy consumption. 

# Results 

![image](https://user-images.githubusercontent.com/70538240/156903450-fc94f4d6-2150-4d62-ad17-d02eb0b25719.png)


Data was fitted, scaled, and applied to the LSTM model, which produced interesting results. 
The average household energy was predicted accurately with a Root Mean Squared Error of 0.624 KiloWatt Hours indicating the model averages an error of + or – 0.624 kWh. 

Using an LSTM model we were able to predict energy consumption for the average household on a given data to less than 1 kWh using previous days given ergy usage, temperature, visibility, and relative humidity. 
The model shows that even with more data, that it is entirely possible to predict energy consumption given specific variables. 

![image](https://user-images.githubusercontent.com/70538240/156903459-f8a426a2-70f9-4cd2-98d5-a875b1fd1cdb.png)






