# Flight Price Prediction System  

This project harnesses the power of machine learning combined with Intel oneAPI to develop a robust system for predicting flight prices. By analyzing various factors such as airline preferences, route specifics, departure and arrival times, and seasonal trends, the model aims to provide accurate price predictions that can help travelers make informed decisions.

# Dataset

![flight_dataset](https://github.com/user-attachments/assets/3a170a07-f0df-4010-8846-dedfc698f8f0)


The dataset consists of multiple flight records with key features, including airline names, journey durations, number of stopovers, departure and arrival times, and routes. These features serve as independent variables, influencing the final price of the tickets.

The dataset is crucial for training the models, allowing them to learn patterns and relationships between flight attributes and ticket prices. Such a model can be instrumental for travel agencies, airlines, and travelers to estimate flight costs and plan bookings efficiently.

​

# oneAPI Integration

​![oneAPI](https://github.com/user-attachments/assets/32727385-2007-4f59-8e1f-1b8fa3f8f7f2)

For performance optimization, I integrated Intel's oneAPI, an open, unified programming model that enables developers to write code that runs seamlessly on multiple hardware types, including CPUs, GPUs, and FPGAs.

Using oneAPI’s oneDAL library, I optimized the Random Forest, Ridge Regression and Scikit-Learn to take advantage of hardware accelerators, leading to faster training and prediction times. This enhancement allows the model to provide real-time predictions with high efficiency, even on large datasets.

​

# Models Used

![pic2](https://github.com/user-attachments/assets/3ea30987-bfa4-49a0-945c-4055c6c4dfc8)

Several machine learning models were used and compared for this task, including:

Random Forest (with oneAPI): A robust ensemble method ideal for handling complex datasets.

Linear Regression: For baseline prediction and comparison.

Decision Tree Regressor: To analyze feature importance and interpretability.

Support Vector Machine (SVR): For capturing nonlinear relationships.

Bagging Regressor: As an ensemble model to improve predictive stability.



Random Forest, optimized with oneAPI, emerged as the most efficient and accurate model. The combination of hardware acceleration and hyperparameter tuning ensured the model performed well under various conditions.

​

# Methodology:

​
Intel oneAPI can significantly enhance a flight price prediction system by utilizing its performance optimization capabilities and support for heterogeneous computing. The following steps outline the key approach:

​
### ✅Data Preparation:

Gather historical flight data, including features such as departure and arrival airports, airline, ticket class, departure time, journey duration, and the flight date.

Handle missing values, perform data cleaning, and preprocess categorical variables using encoding techniques. Ensure that data is split appropriately for training and testing.

​

### ✅Feature Engineering:

Extract meaningful features such as travel month, day of the week, and hour of departure. Create additional features, like holiday indicators or flight distance, to improve prediction accuracy.

Use scaling or normalization for numerical features to optimize model performance.

​

### ✅Model Selection:

Choose machine learning models such as Random Forest Regressor, Decision Tree, Linear Regression, Support Vector Machine (SVR), or Bagging Regressor.

Each model offers a different balance between interpretability, complexity, and accuracy. For high performance, tree-based models like Random Forests are well-suited to complex datasets.

​

### ✅Training and Optimization:

Leverage Intel oneAPI Toolkit and oneDAL (Data Analytics Library) to accelerate training on Intel CPUs, GPUs, or FPGAs.

Utilize parallel processing, vectorization, and threading to improve computation speed and training efficiency, reducing overall runtime.

Perform hyperparameter tuning using methods like RandomizedSearchCV to optimize the models.

​

### ✅Model Evaluation:

Use cross-validation to ensure model robustness. Evaluate the model's performance using metrics such as R² score, MAE, MSE, and RMSE to measure prediction accuracy.

Experiment with different models and feature sets to ensure the optimal configuration for prediction tasks.

​

### ✅Deployment and Monitoring:

Once the best-performing model is identified, deploy it in a production environment, ensuring scalability and real-time prediction capabilities.

Continuously monitor performance and retrain the model with new flight data to maintain prediction accuracy over time.

By utilizing Intel oneAPI technologies, the flight price prediction system benefits from faster training and inference times, allowing for real-time predictions. This approach ensures the system is scalable and capable of efficiently handling large datasets across diverse hardware environments.


# Technologies Used:

​
### Programming Languages: Python

## Libraries and Frameworks:

### scikit-learn: For machine learning models (Random Forest, Linear Regression, Decision Tree, SVR, etc.)

### NumPy & Pandas: For data manipulation and preprocessing

### Matplotlib & Seaborn: For data visualization

### oneDAL (oneAPI Data Analytics Library): For accelerating machine learning models

### Jupyter Notebook: For interactive development

​

# Machine Learning Techniques:

### Random Forest Regressor (with oneAPI optimization)

### Linear Regression, Decision Tree, SVR, Bagging Regressor

### Cross-validation, Hyperparameter Tuning

​

# Tools and Platforms:

### Intel DevCloud: For development and testing with access to hardware accelerators

### oneAPI Toolkit: To enable optimized execution across CPUs, GPUs, and FPGAs

​

# Hardware:

### Intel CPUs: Used for model training and deployment

### GPUs and FPGAs: Accelerated using oneAPI for optimized performance

​
# Results and Discussion

​![pic3](https://github.com/user-attachments/assets/1fdae45e-894e-4c8a-b875-dcc3806fed70)


The optimized Random Forest model provided reliable predictions with a high R² score, demonstrating its ability to capture the complexity of flight pricing patterns. Metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE) were used to assess the model’s accuracy.

​

The Bagging Regressor was saved for future real-time predictions, providing flexibility for dynamic pricing scenarios. The accurate forecasting achieved in this project shows the potential of machine learning models for travel-related applications, such as personalized fare estimation and dynamic pricing recommendations.

​
# Conclusion


This flight price prediction system showcases the benefits of integrating machine learning with oneAPI technology. The optimized Random Forest and scikit-learn models not only achieved high accuracy but also ensured efficient computation across different hardware. Future improvements could involve testing on additional datasets or deploying the system as a real-time pricing API for travel platforms.


​
The project highlights how optimized machine learning solutions can streamline business processes and offer valuable insights, benefiting both service providers and end-users.
