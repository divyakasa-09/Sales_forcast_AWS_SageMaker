

#  **Sales Forecasting using LSTM on AWS SageMaker**  

## **Project Overview**  
This project aims to analyze the impact of weather conditions on burger sales and forecast future sales using an LSTM model. The model is trained and deployed on AWS SageMaker, utilizing data stored in an Amazon RDS MySQL database.  

## **Objectives**  
- Fetch sales and weather data from a MySQL database hosted on Amazon RDS.  
- Analyze whether weather conditions influence burger sales.  
- Train an LSTM model for forecasting sales.  
- Deploy the model as an endpoint using AWS SageMaker for real-time predictions.  

## **Tech Stack**  
### **Languages & Libraries**  
- **Python**  
- **Libraries**: `pandas`, `numpy`, `tensorflow`, `boto3`, `pymysql`, `matplotlib`, `sklearn`, `tarfile`, `keras`, `lightgbm`  

### **Cloud Services & Platforms**  
- **AWS SageMaker** (Model training & deployment)  
- **AWS S3** (Storage for data and models)  
- **Amazon RDS** (MySQL database)  

## **Project Workflow**  
### **1. Data Loading & Exploration**  
- Connect to MySQL database using `pymysql`.  
- Load historical burger sales data.  
- Perform exploratory data analysis (EDA), including visualizations of trends, autocorrelation, and feature importance.  

### **2. Data Preprocessing**  
- Handle missing values and outliers.  
- Normalize the data using `QuantileTransformer`.  
- Windowing the data to prepare it for time-series forecasting.  

### **3. Model Building & Training**  
- Train a baseline model using **LightGBM** to assess feature importance.  
- Develop an **LSTM-based deep learning model** for time-series forecasting.  
- Optimize hyperparameters for improved accuracy.  

### **4. Model Deployment on AWS SageMaker**  
- Save the trained model to **AWS S3** using `boto3`.  
- Deploy the model as a **SageMaker endpoint**.  
- Create an API for real-time inference.  

### **5. Model Inference & Prediction**  
- Make predictions using the deployed endpoint.  
- Evaluate model performance with test data.  




## **Setup & Installation**  
### **1. Install Dependencies**  
Run the following command to install all necessary dependencies:  
```bash
pip install -r requirements.txt
```

### **2. Configure Database Access**  
- Update `Config.yml` with MySQL database credentials:  
```yaml
database:
  host: <your-rds-hostname>
  user: <your-username>
  password: <your-password>
  database: <your-database-name>
```

### **3. Train and Deploy Model on AWS SageMaker**  
#### **Run the Jupyter Notebook (`burger_stores.ipynb`)**  
- Load and preprocess data.  
- Train the **LSTM model**.  
- Deploy the trained model on **AWS SageMaker**.  

#### **Deploy the Model using AWS SageMaker**  
- Save the trained model to **AWS S3**.  
- Use AWS SageMaker to create an endpoint for predictions.  

### **4. Make Predictions**  
- Open `Predict_from_endpoint.ipynb`.  
- Use the deployed SageMaker endpoint for real-time forecasting.  

## **Key Takeaways**  
- Fetching data from **MySQL to Python**.  
- Understanding the impact of weather on sales.  
- Implementing **LSTM models** for time-series forecasting.  
- Deploying ML models on **AWS SageMaker**.  
- Making predictions using SageMaker endpoints.  


## **Key Learnings from this Project**  

This project provided hands-on experience with the end-to-end machine learning workflow, from data acquisition to deployment. The key learnings include:  

1. **Data Extraction & Preprocessing**  
   - Connecting to an **Amazon RDS MySQL database** using `pymysql` to fetch large datasets efficiently.  
   - Handling **time-series data**, performing feature engineering, and normalizing data using **QuantileTransformer**.  

2. **Exploratory Data Analysis (EDA)**  
   - Understanding **autocorrelation and partial correlation** in time-series forecasting.  
   - Identifying **trends, seasonality, and anomalies** in sales data through visualization techniques.  

3. **Model Development**  
   - Implementing a **LightGBM baseline model** to assess feature importance.  
   - Designing and optimizing an **LSTM model** for sales forecasting, including windowing techniques and hyperparameter tuning.  

4. **AWS SageMaker for Model Training & Deployment**  
   - Leveraging **AWS SageMaker** for scalable and efficient model training.  
   - Saving and loading models using **AWS S3**.  
   - Deploying the trained LSTM model as a **SageMaker endpoint** for real-time inference.  

5. **Model Deployment & Serving**  
   - Creating a REST API using **SageMaker Inference Endpoints** to serve predictions.  
   - Making predictions via API calls and testing inference latency.  

6. **Production-Ready Machine Learning Pipeline**  
   - Understanding best practices for deploying ML models in **cloud environments**.  
   - Managing credentials and secure database connections using **config files**.  
   - Exploring **MLOps concepts** for continuous model improvement.  

This project solidified the understanding of **AWS cloud services, time-series forecasting, model deployment, and production ML workflows**. 

## **Future Enhancements**  
- Experimenting with alternative time-series models (e.g., Prophet, Transformer-based models).  
- Implementing real-time data streaming for continuous forecasting.  
- Optimizing AWS SageMaker deployment for cost efficiency.  

