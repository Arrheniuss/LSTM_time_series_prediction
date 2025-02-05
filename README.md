# Time Series Prediction
The project aimed to create, train, and evaluate a recurrent neural network model for analyzing time series data describing air pollution in Beijing from 2013 to 2017. The project focused on a measurement station located near the Wanshou Temple (Wanshouxigong) in the northwestern district of the metropolis.

1. Project Implementation
  - Loadingg the dataset
  - Filling missing data using interpolation
  - Exploratory data analysis
  - Data visualization
  - Standardization of variables using standard scaler for continuous variables and OneHotEncoder for categorical variables
  - Splitting the dataset into training and testing sets in a 90:10 ratio
  - Creating a generator with a 24-Hour time window
  - Creating a neural network model consisting of 2 LSTM layers with (128, 32) units, one Bidirectional LSTM Layer with 64 Units, a Dense Layer with One Unit, and 3 dropout layers at 20%
  - Model evaluation
2. Quality Metrics
  - MSE (train): 635.521
  - MSE (test): 1234.298
  - R^2 (train): 0.903
  - R^2 (test): 0.912
3. Conclusions
- An R² score of 0.91 indicates that the model fits the test data very well. Despite the relatively high Mean Squared Error (MSE), the model effectively explains the variability of PM2.5
- The initial model results were significantly worse before applying the Bidirectional LSTM. As observed, bidirectional networks can greatly improve performance in time series forecasting, where dependencies may be evident in both the past and future
- Outliers may have contributed to the high MSE. Additional filtering or an alternative approach to handling outliers could potentially improve the model's performance
- The application of dropout layers prevented overfitting and allowed the model to achieve good performance on the test data
4. Screenshots
  # PM2.5 Changes Over Time
  ![PM2.5 Changes Over Time](https://github.com/user-attachments/assets/54ec33b4-06d0-451b-a03d-7a54b0eab615)
  # Boxplots of continuous variables
  ![Boxplots of continuous variables](https://github.com/user-attachments/assets/7ba2e489-316b-4d69-82b8-031ca75558fa)
  # Distribution of variables
  ![Image](https://github.com/user-attachments/assets/dc1db612-95ca-481d-8c8c-f05216d638bf)
  # Correlation Map
  ![Image](https://github.com/user-attachments/assets/53d69c6c-6d03-4619-b127-e1f732189201)
  # Model Summary
  ![Image](https://github.com/user-attachments/assets/f9a3a8aa-1eb9-49df-b8f4-d1b0fef04442)
  # Model training process
  ![Image](https://github.com/user-attachments/assets/5765a880-d1a1-4ee9-b6b5-84fa3a940de7)
  # Actual vs. Predicted Values
  ![Image](https://github.com/user-attachments/assets/40e55be7-6746-4445-9890-2c706fa1fd7e)
    
  

