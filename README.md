# 🌿 Air Quality CO Prediction (PySpark & Gradio)

##  Overview
This project predicts **Carbon Monoxide concentration (COGT)** using air quality sensor data and environmental features.  
It combines **Apache Spark (PySpark)** for scalable data processing and **Gradio** for deploying an interactive web application.

Multiple machine learning models were experimented  during development.  
The **best-performing model (Linear Regression with feature scaling)** was selected based on evaluation metrics and deployed.

---

##  Dataset
The dataset used in this project comes from the **UCI Machine Learning Repository**.

🔗 **Dataset Source**:  
https://archive.ics.uci.edu/dataset/360/air+quality

The data contains hourly averaged responses from an array of chemical sensors deployed in an Italian city, along with meteorological information.

### Features include:
- Gas sensor signals (PT08\_S1CO, PT08\_S2NMHC, PT08\_S3NOx, PT08\_S4NO2, PT08\_S5O3)
- Pollutant concentrations (NMHC, C6H6, NOx, NO2)
- Environmental data (Temperature, Relative Humidity, Absolute Humidity)
- Temporal features (hour, day of week, month)

### Target:
- **COGT** – Carbon Monoxide concentration

---

##  Methodology
1. **Data Preprocessing**
   - Removal of non-numeric date/time columns
   - Feature selection and cleaning
   - Handling missing values

2. **Feature Engineering**
   - Vectorization using `VectorAssembler`
   - Normalization using `StandardScaler`

3. **Model Experimentation**
   - Tested several regression models
   - Compared performance using RMSE and R² metrics

4. **Model Selection**
   - Scaled Linear Regression achieved the best performance
   - Chosen for its stability, interpretability, and fast inference

5. **Deployment**
   - Deployed using **Gradio**
   - Interactive interface for real-time predictions

---

##  Gradio Web Interface
The deployed interface allows users to:
- Enter sensor and environmental values
- Get real-time CO concentration predictions
- Use a clean and user-friendly UI

The application is launched directly from **Google Colab** using a public Gradio link.

---

##  Technologies Used
- Python
- Apache Spark (PySpark)
- Spark MLlib
- Scikit-learn
- Gradio
- Google Colab

---

##  Model Performance
- Feature scaling improved model accuracy and stability
- Linear Regression provided consistent results
- Model selection based on:
  - Lowest RMSE
  - Good generalization
  - Fast prediction time

---

##  Author
**Nada**  
AI & Data Science Engineer 

This project demonstrates an end-to-end machine learning pipeline using big data processing, model evaluation, and deployment.
