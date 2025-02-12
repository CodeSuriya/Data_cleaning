# Heart Attack Analysis Project  
This project analyzes global heart attack data, focusing on risk factors like alcohol consumption, diabetes, and medication status.  

GLOBAL DATASET :
It contain the more than 5 million rows.
The python notebook give the clear view of the data cleaning .
In the data cleaning process , I need to handle the missing value , changing the column name , changing the appropriate value in the particular column , changing the datatype int to object 
then finally saving the file into CSV format.


NORTH AMERICA DATASET:
In this dataset , we don't have a north america dataset to analysis for the north america continent.
so we want to create these dataset , that's we use the global dataset .
In global dataset have asia , africa, north america , south america , europe . we separate the north america region category to form the new dataset called north america dataset.
After separate the north america region from the global dataset , we need to check all the elements are correctly updated , in case any missing value or NAN values we need to handle it and fill that value.
Then we need to change the region category north america into united state, canada , mexico..... according to the medical research there are large number of heart attack rate is come from north america (united state . so we need to categorize the region value into 75% of region should be united state , 13% of region should be canada , finally 12% of region should be mexico for the analysis.
Next saved the updated dataset into north america dataset for the final work.


CHINA DATASET:
This repository documents the data cleaning process for the China dataset, which is part of the Heart Attack Analysis Project.
The focus is on preparing the data for further analysis and visualization.
Imported the dataset using pandas and checked the structure.
The 'Blood Pressure' column was in float format.
Converted it into integer values for consistency.
The 'Alcohol Consumption' column had NaN values.
Filled missing values proportionally based on the existing distribution of 'moderate' and 'high' values.
After that process , saved the updated dataset into cleaned china dataset for the final work


FRANCE DATASET:
In the France dataset, I performed a comprehensive data cleaning process to ensure accuracy and consistency for heart attack analysis. Below is a detailed breakdown of the steps I took:

1. Handling Missing Values
Identified and filled missing values in key columns like Alcohol Consumption using proportional imputation based on existing distributions.
Ensured no NaN values remained after processing.

2. Data Type Standardization
Converted categorical values stored as numbers (e.g., Alcohol Consumption) into meaningful labels (Moderate, Heavy).
  
3. Feature Engineering & Categorization
Alcohol Consumption: Defined thresholds (0-14 as Moderate, 15+ as Heavy).
Stress Levels: Binned numerical values into Good, Moderate, and Bad categories.
Air Pollution Levels: Removed the "Bad" category since it contained zero values, keeping only Good and Moderate levels.

4. Column Standardization & Renaming
Renamed columns for clarity (e.g., "Deit_Type" → "Diet_Quality").
Merged Blood Pressure Systolic & Diastolic into a single Blood Pressure column to match the format of the global and China datasets.
Standardized Region Category values from North, South, West, East, Central to:
France (North)
France (South)
France (West)
France (East)
France (Central)

5. Ensuring Data Integrity
Verified all changes using value_counts() and info().
Ensured no unintended NaN values were introduced during transformations.
After that process , saved the updated dataset into cleaned france dataset for the final work


RUSSIA DATASET:

Renaming Columns for Better Readability:
Renamed the "Region" column to "Region_Category" to clarify its purpose.

Standardizing Region Names:
Updated values in the "Region_Category" column to provide better context:
"Rural" → "Russia (Rural)"
"Urban" → "Russia (Urban)"
"Suburban" → "Russia (Suburban)"

Handling Missing Values:
Checked for missing values across all columns.
Decided on appropriate methods to fill or drop missing values based on the column type and impact on analysis.

Converting Categorical Variables to Meaningful Labels:
Converted the "Physical Activity" column from numerical values to categorical labels:
Low → "Bad"
Moderate → "Moderate"
High → "Good"
Converted the "Alcohol Consumption" column:
"Often" → "Moderate"
"Rarely" → "Good"
Converted the "Health Awareness" column (which had numeric values) into meaningful categories.

Dropping Unnecessary Columns:
Removed "Air Pollution Level" as it was not needed for further analysis.

Ensuring Data Type Consistency:
Converted categorical columns (e.g., "Stress Level," "Mental Health," "Physical Activity") to object dtype.
Converted "Daily Water Intake" values into categorical bins for better interpretation.

Final Data Quality Check:
Verified that all transformations were successfully applied.
Ensured there were no remaining NaN values in critical columns.

Outcome:
The Russia dataset is now cleaned, standardized, and ready for analysis.
The cleaned dataset ensures accurate insights for visualizations and comparisons in the final dashboard.



INDIA DATASET:

Handled Missing Values:
Issue: Missing values in the Physical Activity column.
Solution: Imputed missing values using proportional distribution based on existing categories (Good, Moderate, Bad).
Method Used: fillna() with weighted random sampling to maintain dataset balance.

Standardized Column Names:
Issue: Inconsistent column names (spaces, uppercase/lowercase mix).
Solution: Renamed columns using df.columns = df.columns.str.replace(" ", "_").str.lower().
Outcome: Improved readability and consistency.

Categorized Numerical Variables:
Triglyceride Levels: Converted numerical values into Good, Moderate, and Bad categories using defined thresholds.
Blood Oxygen Levels (SpO2%): Classified into Good (>95%), Moderate (90-95%), and Bad (<90%).

Checked for Duplicates:
Issue: Potential duplicate records in the dataset.
Solution: Used df.duplicated().sum() to check for duplicates and removed them using df.drop_duplicates(inplace=True).

Fixed Data Type Issues:
Issue: Columns stored as incorrect data types (e.g., Int64 instead of int64).
Solution: Converted using astype(int).

Detected and Handled Outliers:
Issue: Extreme values in columns like Cholesterol, Blood Pressure, and Heart Rate.
Solution: Used Boxplot to visualize outliers and handled them using IQR method (removed or capped extreme values).


Ensured Logical Consistency:
Issue: Some unrealistic values (e.g., extremely low or high heart rates).
Solution: Applied domain-specific rules to filter out incorrect values.


INDONESIA DATASET

During the data cleaning process for the Indonesia dataset, the following steps were performed to ensure data accuracy, consistency, and completeness:

Handling Missing Values
Checked for missing values using .isnull().sum().
Visualized missing data patterns using msno.matrix().
Used appropriate strategies such as:
Mean/Median Imputation for numerical columns.
Mode Imputation for categorical columns.
Dropping highly null columns if necessary.

Data Type Corrections
Ensured numerical columns were in the correct format (int64 or float64).
Converted categorical columns (e.g., Gender, Diet_Quality, Physical_Activity) to object type if needed.

Handling Duplicates
Checked for duplicate rows using .duplicated().sum().
Removed any duplicate records to maintain data integrity.

Standardizing Categorical Values
Ensured categorical values had a consistent format (e.g., Male vs. M, Female vs. F).
Used .str.lower().str.strip() to standardize text-based categories.

Outlier Detection & Treatment
Used boxplots and histograms to identify potential outliers in key variables (BMI, Blood_Pressure, etc.).
Treated outliers using:
Winsorization (Capping extreme values).
Transformation techniques (Log, Square Root) if required.

Normalization & Scaling (if needed)
Applied Min-Max Scaling or Standardization for numerical variables if analysis required it.

Final Validation & Export
Rechecked dataset using .info() and .describe() to ensure correctness.
Exported the cleaned dataset as cleaned_Indonesia_dataset.csv for further analysis.

Outcome:
🔹 The dataset is now clean, structured, and ready for EDA & visualization. 
🔹 Ensured data integrity, consistency, and accuracy for meaningful insights.


