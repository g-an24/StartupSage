# **StartUp Sage - Startup Success Prediction**

## **Project Overview**  
**StartUp Sage** is a comprehensive machine learning project aimed at predicting the success of startups, defined as the likelihood of acquisition. This project consolidates the entire workflow—from data preparation to model evaluation—into a single, streamlined notebook for seamless analysis and reproducibility.

---

## **Features and Highlights**  
- **Target Variable**: `is_acquired`:
  - **1**: Startup acquired (success).  
  - **0**: Startup not acquired (failure).  
- **Key Features**: Funding metrics, industry categories, founding years, and investment types.  
- **Best Models**: XGBoost and Random Forest with **74% accuracy** and **0.84 ROC-AUC**.  

---

## **Dataset Details**  

### **1. Initial Dataset**  
- **Source**: The dataset, **`updated_investments_VC.csv`** renamed to **`initial_dataset.csv`**, was sourced from Crunchbase.  
- **Description**: Contains raw startup data, including company details, funding history, and operational status.  
- **Key Features**:  
  - `funding_total_usd`: Total funding raised.  
  - `funding_rounds`: Number of funding rounds.  
  - `category_list`: Industry classification.  
  - `status`: Startup operational status (e.g., acquired, closed, operating).  

### **2. Processed Dataset**  
- **Final Dataset**: The preprocessed and engineered dataset, **`df.csv`** renamed to **`encoded_dataset`**, was created from the initial dataset.  
- **Transformations**:  
  - One-hot encoding for categorical variables like founding years and industry categories.  
  - Log transformation for skewed numerical metrics like `funding_total_usd`.  
  - Feature selection using Lasso Regression and tree-based importance metrics.  
- **Size**: Contains **3,695 rows** (startups) and **70 refined features**.  

---

## **Project Structure**  

1. **Notebook**:  
   - All steps—EDA, feature engineering, modeling, and evaluation—are consolidated into a single notebook: **`startup_sage.ipynb`**.  

2. **Workflow Highlights**:  
   - **Data Understanding**: Insightful visualizations and descriptive statistics.  
   - **Feature Engineering**: Creation of key derived features and rigorous encoding.  
   - **Model Training**: Includes Logistic Regression, Random Forest, XGBoost, Neural Networks, and ensemble methods.  
   - **Evaluation**: Comprehensive performance analysis using metrics like Precision, Recall, F1-Score, and ROC-AUC.  

---

## **How to Use**  

1. **Run the Notebook**:  
   - Open **`startup_sage.ipynb`** in Jupyter Notebook or any compatible environment.  
   - Follow the sequential steps to reproduce the results or customize the workflow for new datasets.  

2. **Predict New Data**:  
   - Modify the final section of the notebook to input new startup data.  
   - Use the pre-trained XGBoost model to predict acquisition likelihood (`is_acquired`).  

---

## **Key Insights and Business Impact**  

### **For Investors**:  
- **Focus Areas**: Prioritize startups with consistent funding history and venture-backed investments.  
- **Actionable Insights**: Industry-specific trends (e.g., Technology, Healthcare) guide portfolio strategies.  

### **For Founders**:  
- **Strategic Growth**: Secure multiple funding rounds and align with high-growth sectors.  
- **Benchmarking**: Compare startup metrics against successful benchmarks.  

### **For Accelerators and Policymakers**:  
- **Resource Allocation**: Target startups with early-stage traction and innovative industry alignment.  
- **Global Opportunities**: Foster emerging market ecosystems based on geographic insights.  

---

## **Future Enhancements**  

1. **Text Analysis**:  
   - Integrate NLP techniques to analyze textual data from startup websites and investor reports.  

2. **Geographic Expansion**:  
   - Broaden coverage to include startups from emerging regions like Asia and Africa.  

3. **Real-Time Prediction**:  
   - Develop an automated pipeline for live startup evaluations.  

---

