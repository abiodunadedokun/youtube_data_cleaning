

# **YouTube Data Cleaning Project**

## **Overview**
This project focuses on cleaning and preparing a dataset containing YouTube channel information for meaningful analysis. The raw data included metrics such as subscriber counts, video views, channel rankings, and estimated earnings, but it was riddled with inconsistencies such as missing values, unusual characters, and non-standard formats. The goal of this project was to create a clean, reliable dataset that could be used for data visualization, analysis, or integration into dashboards.

---

## **Objectives**
- Remove inconsistencies and unusual characters to improve data quality.
- Handle missing values effectively for accurate analysis.
- Standardize formats for text, dates, and numerical columns.
- Create a clean dataset ready for further analysis and visualization.

---

## **Dataset**
Raw Youtube data was retrieved from Kaggle.
<img width="958" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/27d2e5bf-b7d2-4a22-ad77-65b4c7825cf5" />


The dataset includes the following key fields:
- `rank`: Channel rank.
- `Youtuber`: Channel name.
- `subscribers`: Total subscribers.
- `video views`: Total video views.
- `category`: Channel category (e.g., Entertainment, Education).
- `channel_type`: Primary type of content.
- `video_views_for_the_last_30_days`: Views in the last 30 days.
- `lowest_monthly_earnings`, `highest_yearly_earnings`: Estimated earnings.
- `created_date`: Date the channel was created.

---

## **Key Data Cleaning Steps**

### **1. Removing Unusual Characters**
- Identified and removed unusual characters from columns such as `Youtuber`, `category`, and `Title`.
- Used regex to ensure only alphanumeric characters and spaces remained.
- **Example**:
  - Before: `MrBe@st`, `Str@nge#Text!`
  - After: `MrBeast`, `StrangeText`

### **2. Handling Missing Values**
- Categorical columns (`channel_type_rank`, `country_rank`) were filled with the most frequent value (mode).
- Missing numerical values in `video_views_for_the_last_30_days` were replaced with logical defaults.

### **3. Standardizing Formats**
- Converted year columns (e.g., `created_year`) to datetime format with default values (e.g., `YYYY-01-01`).
- Removed currency symbols and commas from numerical columns for accurate analysis.

### **4. Ensuring Consistency**
- Checked for duplicates in key fields like `rank` and `Youtuber` to ensure data integrity.
- Verified and corrected data types for all columns (e.g., integers for `subscribers`, strings for `Youtuber`).

---

## **Tools and Technologies**
- **Python**: For scripting the data cleaning process.
- **Pandas**: For data manipulation and handling missing values.
- **Regex (re)**: For identifying and removing unusual characters.
- **Jupyter Notebook**: For iterative development and documentation.

---

## **Results**

<img width="960" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/eb974e7c-f1df-4556-a1c8-d5178072f2ca" />

- All unusual characters removed, ensuring clean and standardized text fields.
- Missing values handled appropriately for analysis-ready data.
- Numerical fields converted to consistent formats for easy calculations.
- Dates standardized to `YYYY-MM-DD` format.

The cleaned dataset is now reliable and suitable for:
- Exploratory data analysis (EDA).
- Creating visualizations and dashboards.
- Predictive modeling or further data processing.


---

## **Future Work**
- Perform exploratory data analysis (EDA) on the cleaned dataset.
- Build interactive dashboards to visualize trends such as top-performing channels, content categories, and viewer engagement.
- Apply machine learning models to predict future subscriber growth.


---
