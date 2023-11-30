# Capstone-Project-3
Bike Sharing

# Bike Sharing

## **Context**

Bike-sharing systems are a new generation of traditional bike rentals where the whole process, from membership, rental, and return back, has become automatic. Through these systems, a user can easily rent a bike from a particular position and return back at another position. Currently, there are about over 500 bike-sharing programs around the world which is composed of over 500 thousand bicycles. Today, great interest exists in these systems due to their important role in traffic, environmental, and health issues.
Apart from interesting real-world applications of bike-sharing systems, the characteristics of data generated by these systems make them attractive for research. Unlike other transport services such as buses or subways, the duration of travel, departure, and arrival position is explicitly recorded in these systems. This feature turns the bike-sharing system into a virtual sensor network that can be used for sensing mobility in the city. Hence, it is expected that the most important events in the city could be detected by monitoring these data.<br>

## **Business Problem**

How much bikes that must be provided by the rental company? <br>
This must be solved so the rental company is having enough bike to be rent. <br>
Also if it's not solved, there might be stock shortage of bike to be rent.

## **Business Task**

To predict the number of bikes that must be provided by the rental company. So we use model(regression) to predict the number of bikes.<br>

## **Metric Evaluation**

Mean Absolute Error : To Predict Absolute Value of Error that the rental company need to adjust.

## **Project Limitations**

The moodel only can predicting amount of rent bike with total less than 970. So above that, the model can't predicting it.<br>

## **Available Data**

From https://capitalbikeshare.com/system-data /  data_bike_sharing.csv file, and here the dictionary:<br>

## **Features**

- dteday: date
- season: season (1: winter, 2: spring, 3: summer, 4: fall)
- hr: hour (0 to 23)
- holiday: holiday or not
- temp: normalized temperature in Celsius. The values are derived via (t-tmin)/(tmax-tmin), tmin=-8, t_max=+39 (only in hourly scale)
- atemp: Normalized feeling temperature in Celsius. The values are derived via (t-tmin)/(tmax-tmin), tmin=-16, t_max=+50 (only in hourly scale)
- hum: normalized humidity. The values are divided into 100 (max)
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered
- weathersit:
    1. Clear, Few clouds, Partly cloudy, Partly cloudy
    2. Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    3. Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    4. Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog

## **To Do List**

- EDA
- Feature Engineering
- Modelling
- Prediction
- Feature Importances
- Conclusion & Recommendation

## Data Understanding

- Capital Bikeshare is bikesharing program by The District Department of Transportation (DDOT)’s America. They have partnership with Arlington County, the City of Alexandria, Montgomery County, Fairfax County, Prince George's County, and the City of Falls Church.<br>
- With Capital Bikeshare we can take a bicycle from more than 700 stations across the Washington, DC, metro region and return it to any station near our destination. Check out a bike for our trip to work, Metro, run errands, go shopping, or visit friends and family.<br>
- Capital Bikeshare is also the successor to DDOT's first bikesharing system called Smartbike DC, which launched in August 2008 with ten stations and 100 bikes.<br>
- DDOT updated its plan for the District’s portion of the Capital Bikeshare system in 2020. This plan was drafted to create goals for the program, describe measures that track progress toward goal achievement, analyze how well the system is performing, generate system expansion scenarios and financial forecasts for the near term, and recommend an expansion strategy for the next six years that best meets the goals and addresses system performance gaps. 


# **NOTE**

To FIND **CNT** we need to combine 2 model, 1 for casual and 1 for registered.<br>

So, `Y_prediction_cnt` = y_prediction_casual + y_prediction_registered

ALSO model is to large to upload, so we compressing it. So we need to unzip first to use the model.

- model_registered-stackreg_BikeSharing.sav.zip
- model_casual-stackreg_BikeSharing.sav.zip
