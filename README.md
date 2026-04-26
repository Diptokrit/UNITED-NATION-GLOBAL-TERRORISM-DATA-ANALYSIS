#  United Nation Global Terrorism Dataset Analysis 

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
## 🔄 Project Workflow

The overall workflow of the project follows a structured sequence, starting from raw data and ending with final insights and visualization.

The process begins with data collection and understanding the structure of the dataset. This is followed by data preprocessing, where missing values are handled, relevant features are selected, and the data is cleaned to ensure consistency.

Once the data is prepared, exploratory data analysis (EDA) is performed to identify trends, distributions, and patterns in the dataset. This step helps in building an initial understanding and guides further analysis.

After EDA, the data is transformed into suitable formats for machine learning. Transaction-based formatting is used for association rule mining, while numerical encoding is applied for clustering techniques.

Next, unsupervised machine learning algorithms such as Apriori, FP-Growth, and K-Means are applied to uncover hidden patterns, relationships, and groupings within the data.

The results obtained from these models are then analyzed and interpreted to extract meaningful insights. Finally, all the findings are visualized using a Power BI dashboard, which allows users to interact with the data and explore different aspects of the analysis.

This step-by-step workflow ensures that the project moves logically from raw data to actionable insights.

<img width="2030" height="1214" alt="image" src="https://github.com/user-attachments/assets/a383ad48-a979-40db-af25-02f91340b1dd" />



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

### 🔗 Apriori Algorithm 

- Converted data into a **transaction format**  
- Generated **frequent itemsets**  
- Created association rules using:
  - Support  
  - Confidence  
  - Lift  

**Purpose:**  
To identify relationships between **weapon types and target types**.

The Apriori algorithm was used to identify relationships between different features in the dataset, particularly between weapon types and target types.

To apply this method, the data was first converted into a transaction-based format, where each record represents a combination of attributes. The algorithm then scanned the data to find frequently occurring itemsets based on a minimum support threshold.

Once the frequent itemsets were generated, association rules were created to understand how strongly different variables are related to each other. These rules were evaluated using key metrics such as support, confidence, and lift, which help measure the frequency and strength of the relationships.

This approach made it possible to identify meaningful patterns, such as which types of weapons are commonly associated with specific targets, indicating that these events follow certain structured behaviors rather than occurring randomly.
---

### ⚡ FP-Growth Algorithm

- Built an **FP-Tree structure**  
- Extracted frequent patterns efficiently  
- Generated association rules  

The FP-Growth algorithm was applied as an alternative to the Apriori method to efficiently identify frequent patterns in the dataset.

Instead of generating multiple candidate itemsets like Apriori, this approach uses a compact data structure known as an FP-Tree. This allows the algorithm to scan the dataset more efficiently and extract frequent patterns without excessive computation.

Once the frequent patterns were identified, association rules were generated in a similar way, helping to understand the relationships between different variables.

The main advantage of using FP-Growth was its efficiency, especially when working with larger datasets. It also helped in validating the patterns discovered using the Apriori algorithm, ensuring that the results were consistent and reliable.

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

### K-Means Clustering

K-Means clustering was applied to group similar patterns within the dataset and explore whether attacks could be categorized into distinct clusters.

Since the algorithm requires numerical input, categorical features such as weapon type and target type were first converted into numerical values using label encoding. After preprocessing, the model was trained using K = 3 to divide the data into three clusters.

The goal of this approach was to identify underlying groupings in the data and understand whether certain types of attacks share similar characteristics.

However, it was observed that clustering was not as effective as association rule mining in this case. This is mainly because the dataset is largely categorical, and converting it into numerical form does not always preserve meaningful relationships between categories.
---

## 📈 Power BI Dashboard

An interactive dashboard was created using Power BI to present the findings in a clear and user-friendly way.

### Dashboard Features:

- **KPI Cards** → Total attacks, total kills, total wounded, and successful attacks  
- **Filters (Slicers)** → Year, Region, and Attack Type  
- **Map Visualization** → Global distribution of attacks   
- **Bar Charts** →  
  - Attacks by region  
  - Attack type distribution  
- **Line Chart** → Trend of attacks over time  
- **Donut Chart** → Target distribution   
- **Insights Section** → Key findings summarized  

The dashboard allows users to **interactively explore the data and understand patterns easily**.

---

## 📈 Key Insights

- Terrorist attacks increased significantly after 2010 and peaked around the mid-2010s  
- Attacks are concentrated in specific regions such as the Middle East and South Asia  
- Bombing and explosive attacks are the most commonly used methods  
- Private citizens are the most frequently targeted group  
- Strong relationships exist between weapon types and target categories

From the overall analysis, several important patterns were observed. It was found that terrorist attacks increased significantly after 2010 and reached a peak around the mid-2010s, indicating a period of intensified activity.

The data also showed that attacks are not evenly distributed across the world, but are concentrated in specific regions, particularly the Middle East and South Asia. This highlights the regional nature of such incidents.

In terms of attack methods, bombing and explosive-based attacks were found to be the most commonly used, suggesting a preference for high-impact strategies. Additionally, private citizens were identified as the most frequently targeted group, indicating that many attacks are aimed at causing widespread public fear.

The machine learning analysis further revealed that there are strong relationships between weapon types and target categories, confirming that these incidents follow certain patterns rather than occurring randomly.

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

This project was implemented using a combination of Python-based tools for data analysis and Power BI for visualization.

Python was used for data preprocessing, analysis, and model implementation. Libraries such as Pandas were used for handling and manipulating the dataset, NumPy was used for performing numerical operations, and Matplotlib was used to create basic visualizations during the exploratory analysis phase.

For the machine learning part, Scikit-learn was used to implement the K-Means clustering algorithm, while the MLxtend library was used to apply Apriori and FP-Growth algorithms for association rule mining.

Finally, Power BI was used to design and develop an interactive dashboard, allowing the insights to be presented in a clear and visually appealing way.
---

## 📷 Dashboard Preview

<img width="1726" height="971" alt="image" src="https://github.com/user-attachments/assets/536f116b-e10e-4de7-bd9a-859622a89aee" />

---

## 👤 Author

- Name: Diptokrit Chowdhury 
- LinkedIn: [https://www.linkedin.com/in/diptokrit-chowdhury-38b7b327a/]  

---

## 📌 Conclusion

This project demonstrates how combining data preprocessing, exploratory data analysis, machine learning, and visualization can help transform raw and complex data into meaningful insights.

Through the analysis of global terrorism data, it was possible to understand how attack patterns have evolved over time and how they vary across different regions. The exploratory analysis helped in identifying major trends, such as the rise in attacks during certain periods and the concentration of incidents in specific parts of the world.

Applying machine learning techniques added another layer to the analysis. The use of association rule mining made it possible to identify relationships between weapon types and target categories, showing that these incidents often follow certain patterns rather than occurring randomly. Clustering was also explored to group similar attack behaviors, which provided additional perspective, even though it was less effective due to the nature of the data.

The Power BI dashboard played an important role in presenting these findings in a clear and interactive way. Instead of just looking at static results, users can explore the data through filters, maps, and charts, making it easier to understand the insights and patterns discovered during the analysis.

Overall, this project highlights the importance of a structured and step-by-step approach to data analysis. By combining different techniques and tools, it becomes possible to gain a deeper understanding of real-world datasets and uncover insights that are not immediately obvious.

---
