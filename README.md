# 🌍 Global Terrorism Analysis Dashboard

---

## 📌 Objective

The main objective of this project is to analyze global terrorism data in order to understand how attack patterns have evolved over time and how they vary across different regions, targets, and methods.

This project is designed not just to visualize the data, but to explore it in depth and extract meaningful insights using both analytical and machine learning approaches.

The project aims to:

- Identify key trends and long-term patterns in terrorist activities  
- Analyze how attacks are distributed geographically and which regions are most affected  
- Discover relationships between weapon types and target categories  
- Apply unsupervised machine learning techniques to uncover hidden patterns  
- Present all findings through an interactive Power BI dashboard  

---

## 📊 Dataset Overview

This project uses the **Global Terrorism Database (GTD)**, which contains detailed records of terrorist incidents across the world.

The dataset spans multiple years and includes incidents from various countries and regions, making it suitable for both trend analysis and pattern discovery.

The dataset includes:

- Attack types (e.g., bombing/explosion, armed assault, assassination)  
- Target types (e.g., private citizens, military, government, police)  
- Geographic information (region and country)  
- Casualty details (number of people killed and wounded)  

This rich dataset allows for both **exploratory data analysis and machine learning-based insights**.

---

## 🧹 Data Pre-Processing 

Before performing analysis, the dataset was cleaned and prepared carefully to ensure accuracy and consistency.

The following steps were performed:

- Missing values were identified and handled appropriately  
- Relevant columns were selected such as:
  - `weaptype1_txt`
  - `targtype1_txt`
  - `region_txt`
  - `iyear`
- Categorical data was standardized for consistency  
- Unnecessary or irrelevant data was removed  

This step ensured that the dataset was **clean, structured, and ready for further analysis**.

---

## 📊 Exploratory Data Analysis (EDA)

EDA was performed to understand the structure and behavior of the dataset.

The analysis included:

- **Trend Analysis** → Studying how attacks changed over time  
- **Regional Analysis** → Identifying regions with the highest number of attacks  
- **Attack Type Distribution** → Understanding the most common attack methods  
- **Target Analysis** → Identifying frequently targeted groups  

These analyses helped in identifying **initial patterns and gaining insights into the data**.

The exploratory data analysis (EDA) phase was carried out to better understand the dataset and identify meaningful patterns within the data.

During this stage, the overall trend of attacks over the years was analyzed to observe how terrorist activities have increased or decreased over time. This helped in identifying periods where there was a noticeable rise in incidents.

A region-wise analysis was also performed to understand which parts of the world are most affected. This made it clear that attacks are not evenly distributed and are concentrated in specific regions.

The distribution of attack types was studied to identify the most commonly used methods. It was observed that certain types of attacks occur more frequently, indicating preferred strategies.

Similarly, target analysis was conducted to understand which groups are most frequently affected. This helped in identifying that certain categories, such as civilians, are targeted more often.

In addition to these, comparisons were made between different variables to understand how they relate to each other. Patterns such as repeated combinations of weapons and targets were also observed, which later supported the machine learning analysis.

Overall, this step helped in building a clear understanding of the data and provided a strong foundation for applying machine learning techniques in the next stage.

---

## 🤖 Unsupervised Machine Learning

Since the dataset does not contain predefined labels, **unsupervised learning techniques** were applied to discover hidden patterns.

---

### 🔗 Apriori Algorithm (Association Rule Mining)

- Converted data into a **transaction format**  
- Generated **frequent itemsets**  
- Created association rules using:
  - Support  
  - Confidence  
  - Lift  

**Purpose:**  
To identify relationships between **weapon types and target types**.

---

### ⚡ FP-Growth Algorithm

- Built an **FP-Tree structure**  
- Extracted frequent patterns efficiently  
- Generated association rules  

**Purpose:**  
To improve performance and validate patterns found using Apriori.

---

### 🎯 K-Means Clustering

- Converted categorical data into numerical form using **Label Encoding**  
- Applied clustering (K = 3)  
- Grouped similar attack patterns into clusters  

**Purpose:**  
To identify **hidden groupings and similarities in attack behavior**.

**Observation:**  
Clustering was less effective compared to association rule mining due to the categorical nature of the dataset.

---

## 📈 Power BI Dashboard

An interactive dashboard was created using Power BI to present the findings in a clear and user-friendly way.

### Dashboard Features:

- **KPI Cards** → Total attacks, total kills, total wounded, and successful attacks  
- **Filters (Slicers)** → Year, Region, and Attack Type  
- **Map Visualization** → Global distribution of attacks 🌍  
- **Bar Charts** →  
  - Attacks by region  
  - Attack type distribution  
- **Line Chart** → Trend of attacks over time 📉  
- **Donut Chart** → Target distribution 🍩  
- **Insights Section** → Key findings summarized  

The dashboard allows users to **interactively explore the data and understand patterns easily**.

---

## 📈 Key Insights

- Terrorist attacks increased significantly after 2010 and peaked around the mid-2010s  
- Attacks are concentrated in specific regions such as the Middle East and South Asia  
- Bombing and explosive attacks are the most commonly used methods  
- Private citizens are the most frequently targeted group  
- Strong relationships exist between weapon types and target categories  

---

## 🛠️ Tools & Technologies

- **Python**  
  - Pandas (data handling)  
  - NumPy (numerical operations)  
  - Matplotlib (visualization)  

- **Machine Learning**  
  - Scikit-learn (K-Means clustering)  
  - MLxtend (Apriori and FP-Growth)  

- **Power BI** → Dashboard creation and visualization  

---

## 📷 Dashboard Preview

![Dashboard Screenshot](dashboard/dashboard_screenshot.png)

---

## 🔗 Project Links

- 📊 **Power BI Dashboard**: [Paste Google Drive Link]  
- 📓 **Google Colab Notebook**: [Paste Link]  
- 💻 **GitHub Repository**: [Paste Link]  

---

## 👤 Author

- Name: Your Name  
- LinkedIn: [Paste your LinkedIn link]  

---

## 📌 Conclusion

This project demonstrates how combining data preprocessing, exploratory analysis, machine learning, and visualization can transform raw data into meaningful insights.

By analyzing global terrorism data, we were able to identify trends, uncover relationships, and understand patterns that are not immediately visible.

The integration of a Power BI dashboard further enhances usability by allowing users to explore the data interactively and gain deeper insights.

---
