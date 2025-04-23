Project Title:
Traffic Speed Forecasting Using LSTM
Author: Cyrus White

Description and Objective:
This project aims to forecast daily average traffic speeds using historical data and machine learning. By training a Long Short-Term Memory (LSTM) neural network on 2015 traffic data from Los Angeles, along with weather and calendar-based features, the goal was to predict the next day’s traffic speed and identify days likely to experience higher congestion. The objective was to explore how time-series modeling can support traffic planning and congestion detection.

Dataset Used:
The dataset used in this project includes one full year (2015) of daily traffic speed records, paired with daily weather conditions (temperature and precipitation), U.S. federal holidays, and derived calendar features such as weekends and day of the week. The data was preprocessed and merged manually from multiple sources.

Model/Method Overview:
The model is a sequential LSTM neural network with two LSTM layers (64 and 32 units), followed by dropout layers to prevent overfitting, and a dense output layer for single value prediction. It takes sequences of 30 days of data to predict the speed on the 31st day. The model was trained using the Adam optimizer with early stopping and a validation split.

Instructions to Run the Code:

Upload Traffic_Weather_Holiday_2015.xlsx to the /data/ directory.

Open and run the notebook located in /notebooks/final_model.ipynb.

The notebook will load the data, train the model, make predictions, and display results automatically. Output plots and top congestion days will be saved to /results/.

Summary of Results and Key Findings:
The model achieved a Mean Absolute Error (MAE) of 7.76 mph and a Root Mean Squared Error (RMSE) of 9.63 mph. While the R² score was low (-0.0678), the model achieved a practical accuracy of 71.43% within ±10 mph of the actual speeds. These results indicate that the model can identify general traffic patterns and trends, especially slower traffic days, making it a useful tool for long-term planning and forecasting.
