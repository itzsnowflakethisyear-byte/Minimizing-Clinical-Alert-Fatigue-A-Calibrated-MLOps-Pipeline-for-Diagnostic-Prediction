## **Exploratory Data Analysis of a Healthcare Dataset**

**Tools:** Python (pandas, NumPy), SQL-style analysis, Matplotlib/Seaborn, Data Visualization
**Domain:** Healthcare Operations, Cost Optimization, Quality of Care

This project performs exploratory data analysis (EDA) on a synthetic healthcare dataset to uncover patterns related to patient demographics, medical conditions, billing, and test results, and to assess the data's suitability for predictive modeling

### **Dataset**
The project utilizes a  healthcare dataset where each column provides specific information about the patient, their admission, and the healthcare services provided, making this dataset suitable for various data analysis and modeling tasks in the healthcare domain. Here's a brief explanation of each column in the dataset 

### **Problem Statement**
The primary objective was to identify meaningful associations, assess data quality, and determine if the dataset supports modeling. Key questions explored:
- How test results and billing amounts vary across different medical conditions? 
- Which conditions, admission types, and demographics associate with abnormal results? 
- Under what circumstances do negative billing amounts occur? 
- Which insurance providers perform best in terms of normal test results? 

### **Key Insights**
- **Uniformity:** Overall, categories for variables like age, gender, medical conditions, admission types, and test results are evenly distributed, providing a balanced dataset.
- **Condition & Outcomes:** Cancer, Diabetes, and Obesity tend to have more abnormal test results, while Hypertension and Asthma show slightly higher normal results.
- **Billing Drivers:** Cancer treatments have the highest typical billing amounts, making them financially heavy to treat.
- **Primary Drivers of Abnormal Results:** The severity of a patient's condition at the time of admission is the primary driver of abnormal outcomes, not age or gender. Emergency admissions consistently have the highest risk.
- **Rare Negative Billing:** Negative billing amounts are concentrated in specific insurer-admission combinations and are likely corrections or disputes, not routine adjustments.
- **Provider Performance Variation:** No single insurer is consistently the best across all conditions. UnitedHealthcare leads in 4 of 6 conditions, but overall performance varies, suggesting inconsistent care outcomes in some areas.

### **Important Visualizations**
Age Distribution Plot: The sns.histplot of patient_df['Age'] showing the uniform distribution 
Admissions by Medical Condition Plot: The bar plot of patient_df['Medical Condition'].value_counts() to illustrate balance
Billing Amount Boxplot by Medical Condition: The boxplot showing how billing costs vary, highlighting Cancer's high bills
Proportion of Test Results by Age Group: The bar plot showing that younger patients have a higher likelihood of normal results 
Abnormal Test Rate by Age Group for Key Conditions: The line plot illustrating that Cancer requires consistent monitoring across all ages 
Top Insurance Provider per Medical Condition: The bar plot that labels which insurer performs best for each condition based on normal test results 

### **Stakeholder Takeaway**

Hospital administrators and insurance providers should recognize that admission acuity significantly impacts test outcomes more than demographics. While UnitedHealthcare performs strongly across several conditions, the variability in outcomes for Cancer and Obesity across providers indicates a need for better care standardization. Negative billing is a minor, specific issue likely related to reconciliation processes.

### **Actionable Recommendations**

- **Focus on Care Pathways:** Implement initiatives to improve care pathways for emergency and urgent admissions to reduce abnormal outcomes.
- **Implement Early Screening:** Roll out targeted early screening programs for Cancer and Diabetes, as age alone is not a reliable risk indicator.
- **Standardize Care:** Collaborate with underperforming insurers in high-variability conditions like Cancer and Obesity to standardize treatment protocols and improve outcome consistency. 
- **Enhance Data for Future Modeling:** To build effective predictive models, plan for data enrichment or collection of more granular clinical data to improve the signal-to-noise ratio.
