# Customer Lifetime Value Prediction Using BigQuery  

## Overview  
Customer Lifetime Value (CLV) prediction is essential for businesses to understand the long-term value of their customers. This project, completed as part of the **GCCF Course Lab Work**, utilizes **Google BigQuery** for large-scale data processing and analysis to predict CLV efficiently. By leveraging **machine learning techniques** and **SQL-based feature engineering**, the model estimates the revenue a customer is expected to generate over time.  

## Features  
- **BigQuery for data storage & processing**: Handles large-scale customer data efficiently.  
- **Data preprocessing & transformation**: Cleans and prepares data for modeling.  
- **Feature engineering**: Extracts meaningful insights to improve prediction accuracy.  
- **Machine learning model training**: Uses regression techniques to predict CLV.  
- **Performance evaluation & visualization**: Assesses model accuracy and business impact.  

## Technologies Used  
- **Google BigQuery**  
- **Python** (Pandas, NumPy, Scikit-learn)  
- **Jupyter Notebook**  
- **SQL** for data transformation  
- **Matplotlib, Seaborn** for visualization  

## Brief Explanation  
The project follows these steps:  
1. **Data Extraction**: Retrieves customer transaction data from **BigQuery**.  
2. **Data Cleaning & Preprocessing**: Handles missing values, duplicates, and outliers.  
3. **Feature Engineering**: Constructs relevant customer metrics (e.g., recency, frequency, monetary value).  
4. **Model Selection & Training**: Applies ML models (e.g., **Linear Regression, Decision Trees**) for CLV prediction.  
5. **Evaluation & Business Insights**: Analyzes results, visualizes trends, and suggests marketing strategies.  

## Outcomes  
- **Accurate CLV predictions** to help businesses optimize marketing budgets.  
- **Segmentation of customers** based on predicted lifetime value.  
- **Improved customer retention strategies** by identifying high-value customers.  
- **Enhanced decision-making** using data-driven insights from BigQuery.  

## Installation & Setup  
1. Clone the repository:  
   ```bash
   git clone https://github.com/NettamCharansai/Customer-Lifetime-Value-Prediction.git  
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt  
   ```
3. Set up Google Cloud authentication:  
   ```bash
   export GOOGLE_APPLICATION_CREDENTIALS="path/to/your-service-account.json"
   ```
4. Run the Jupyter Notebook:  
   ```bash
   jupyter notebook  
   ```

## Usage  
- Open **Customer-Lifetime-Value-Prediction.ipynb**  
- Run the notebook step-by-step  
- Modify SQL queries based on dataset requirements  

## Contribution  
This project was completed as part of the **GCCF Course Lab Work**. Contributions are welcome! Feel free to fork the repo and submit pull requests.  

## License  
This project is licensed under the **MIT License**.  
