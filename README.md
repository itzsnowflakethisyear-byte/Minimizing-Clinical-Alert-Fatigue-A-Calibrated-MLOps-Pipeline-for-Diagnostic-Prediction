Exploratory Data Analysis of a Healthcare Dataset
This project performs exploratory data analysis (EDA) on a synthetic healthcare dataset to uncover patterns related to patient demographics, medical conditions, billing, and test results, and to assess the data's suitability for predictive modeling (p. 1).
Dataset
The project utilizes a synthetic healthcare dataset provided as cleaned_healthcare_dataset.csv. The dataset contains approximately 55,000 patient records (p. 3) and includes features such as:
Age (range 13-89 years) (p. 3) and Gender (nearly 50/50 split) (p. 3)
Medical Condition (Arthritis, Diabetes, Cancer, etc., all uniformly represented) (p. 4)
Admission Type (Emergency, Urgent, Elective, all in similar proportions) (pp. 4-5)
Insurance Provider
Billing Amount (including rare negative values) (pp. 1, 17)
Test Results (Normal, Abnormal, Inconclusive, evenly represented) (p. 5)
Date of Admission and Discharge Date (p. 2)
Problem Statement
The primary objective was to identify meaningful associations, assess data quality, and determine if the dataset supports modeling (p. 1). Key questions explored:
How test results and billing amounts vary across different medical conditions? (pp. 6-7)
Which conditions, admission types, and demographics associate with abnormal results? (p. 12)
Under what circumstances do negative billing amounts occur? (p. 17)
Which insurance providers perform best in terms of normal test results? (pp. 19, 22)
Key Insights
Uniformity: Overall, categories for variables like age, gender, medical conditions, admission types, and test results are evenly distributed, providing a balanced dataset (pp. 3-6).
Condition & Outcomes: Cancer, Diabetes, and Obesity tend to have more abnormal test results, while Hypertension and Asthma show slightly higher normal results (p. 7).
Billing Drivers: Cancer treatments have the highest typical billing amounts, making them financially heavy to treat (p. 8).
Primary Drivers of Abnormal Results: The severity of a patient's condition at the time of admission is the primary driver of abnormal outcomes, not age or gender (pp. 14, 16). Emergency admissions consistently have the highest risk (p. 14).
Rare Negative Billing: Negative billing amounts are concentrated in specific insurer-admission combinations and are likely corrections or disputes, not routine adjustments (pp. 17, 19).
Provider Performance Variation: No single insurer is consistently the best across all conditions. UnitedHealthcare leads in 4 of 6 conditions, but overall performance varies, suggesting inconsistent care outcomes in some areas (pp. 23, 27).
Modeling Readiness: The dataset is well-suited for descriptive insights but has a low signal-to-noise ratio, limiting its immediate use for robust predictive modeling without additional data enrichment (p. 27).
Important Visualizations
To support the key insights in the README, you should include the following visualizations from the notebook:
Age Distribution Plot: The sns.histplot of patient_df['Age'] showing the uniform distribution (p. 3).
Admissions by Medical Condition Plot: The bar plot of patient_df['Medical Condition'].value_counts() to illustrate balance (p. 4).
Billing Amount Boxplot by Medical Condition: The boxplot showing how billing costs vary, highlighting Cancer's high bills (p. 8).
Proportion of Test Results by Age Group: The bar plot showing that younger patients have a higher likelihood of normal results (p. 10).
Abnormal Test Rate by Age Group for Key Conditions: The line plot illustrating that Cancer requires consistent monitoring across all ages (p. 16).
Top Insurance Provider per Medical Condition: The bar plot that labels which insurer performs best for each condition based on normal test results (pp. 22-23).
Stakeholder Takeaway
Hospital administrators and insurance providers should recognize that admission acuity significantly impacts test outcomes more than demographics. While UnitedHealthcare performs strongly across several conditions, the variability in outcomes for Cancer and Obesity across providers indicates a need for better care standardization. Negative billing is a minor, specific issue likely related to reconciliation processes.
Actionable Recommendations
Focus on Care Pathways: Implement initiatives to improve care pathways for emergency and urgent admissions to reduce abnormal outcomes (pp. 14, 16).
Implement Early Screening: Roll out targeted early screening programs for Cancer and Diabetes, as age alone is not a reliable risk indicator (pp. 16-17).
Standardize Care: Collaborate with underperforming insurers in high-variability conditions like Cancer and Obesity to standardize treatment protocols and improve outcome consistency (p. 27).
Enhance Data for Future Modeling: To build effective predictive models, plan for data enrichment or collection of more granular clinical data to improve the signal-to-noise ratio (p. 27).
