#  Data Cleaning & Insights Generation on Surat's Housing Dataset  

This project focuses on cleaning and analyzing a housing dataset from Surat, India, to derive meaningful insights for potential buyers, sellers, and real estate stakeholders.  

The raw dataset contained inconsistencies, missing values, and outliers, which were systematically cleaned using Python (Pandas, NumPy). Once cleaned, the dataset was explored to uncover meaningful patterns and trends in Surat’s real estate market, including property type distributions, location-based pricing, and the relationship between property size and price per square foot.  

---

##  Data Cleaning Process  

The raw dataset contained multiple inconsistencies, missing values, and unrealistic entries that needed to be addressed before meaningful analysis. The following steps were performed:  

### 1️⃣ Handling Missing Values  
- Identified columns with null or incomplete data.  
- Removed rows with excessive missing fields to ensure quality.  
- Retained missing rows in the `description` column since they contained other relevant attributes.  
- Numerical missing values were imputed where possible, while non-recoverable rows were dropped.  

---

### 2️⃣ Removing Duplicates  
- Duplicate property listings were identified and removed.  
- This step ensured that the dataset reflected unique property records, avoiding skewed insights.  

---

### 3️⃣ Converting Data Types  
- In the raw dataset, all columns were stored as `object` data type.  
- Converted relevant columns to proper types:  
  - Prices and square feet → numeric.  
  - Dates → datetime.  
  - Categorical attributes (e.g., property type, furnishing) → category.  
- This conversion allowed for accurate computation, filtering, and statistical modeling.  

---

### 4️⃣ Creating New Columns  
- **Floors Column Transformation**: The raw format was `"x out of y"` (e.g., *5 out of 12*). This was split into two new columns:  
  - `floor_number` = x (current floor).  
  - `total_floors` = y (total building floors).  
  This helps in analyzing **floor-level premiums** and building size effects.  

- **Price Column Transformation**: The raw column had values like `"84 Lac"` or `"1.2 Cr"`. A new column `price_num` was created to convert these into numeric values (e.g., `84,00,000`).  
  - This makes price values consistent and suitable for statistical modeling.  

---

### 5️⃣ Handling Outliers  
- **Floor Column Outliers**: Removed irrelevant or nonsensical values.  
- **Price & Price per Sq. Ft.**: Detected extreme outliers (e.g., unrealistic per-square-foot rates). These were removed to improve accuracy.  
- **Furnishing Column Outliers**: Removed rare/unstandardized entries that didn’t fit into logical furnishing categories.  

---

##  Insights & Findings  

Once the dataset was cleaned, exploratory data analysis (EDA) was performed to uncover meaningful insights.  

### 1️⃣ Average Price per Square Foot  
- The average price per sq. ft. in Surat was found to be **₹4926.61**.  
- This serves as a benchmark for evaluating whether a property is overpriced or undervalued compared to city averages.  

---

### 2️⃣ Locality-wise Pricing  
- Localities with the highest average price per sq. ft. represent premium markets, often with better infrastructure, schools, and amenities.  
- Localities with the lowest averages indicate affordable or emerging markets with potential growth opportunities.  

---

### 3️⃣ Correlation between Square Feet & Price per Sq. Ft.  
- A correlation of **0.556** was observed, suggesting a moderate positive relationship.  
- **Interpretation**:  
  - Larger properties tend to command a higher price per sq. ft.  
  - Reflects demand for **premium, spacious homes** in Surat.  
  - However, since the correlation isn’t very strong (not close to 1), exceptions exist—location, amenities, and property type also play key roles.  

---

### 4️⃣ New vs. Resale Properties  
- New properties were found to be more expensive than resale properties.  
- This premium pricing can be attributed to modern amenities, newer construction standards, and high demand for brand-new homes.  

---

### 5️⃣ Super Built-up vs. Carpet Area Homes  
- Homes listed with super built-up area pricing were observed to have higher average price per sq. ft.  
- This reflects the inclusion of shared/common spaces (e.g., lifts, corridors) in pricing, which drives up the per sq. ft. cost.  

---

### 6️⃣ Construction Status: Ready-to-Move vs. Under Construction  
- **Under Construction Properties** → Higher average price per sq. ft.  
  - Buyers pay a premium anticipating **future value appreciation**.  
- **Ready-to-Move Properties** → Lower average per sq. ft. pricing.  
  - More affordable but with less appreciation potential.  

- **Market Share**:  
  - Ready-to-Move: **62.89%** of listings.  
  - Under Construction: **37.11%** of listings.  

---

### 7️⃣ Furnishing Status & Pricing  
- **Unfurnished Properties**:  
  - Highest price per sq. ft.  
  - Typically **larger homes**, appealing to premium buyers who customize interiors.  

- **Semi-Furnished Properties**:  
  - Lowest price per sq. ft.  
  - Typically smaller homes, targeted at budget-conscious buyers.  

---

### 8️⃣ Floor-Level Premiums  
- **Higher Floors**:  
  - Generally command a premium due to better views, reduced noise, and improved ventilation.  
- **Taller Buildings**:  
  - Higher total floors correlated with increased per sq. ft. prices, suggesting demand for high-rise living.  

---

##  Key Takeaways  

-  Surat’s housing market is dominated by ready-to-move apartments, but under-construction projects are priced higher per sq. ft..  
-  **Locality strongly influences property pricing**, with premium neighborhoods far outpacing affordable zones.  
-  Unfurnished, larger homes are the most expensive per sq. ft., while semi-furnished, smaller homes are the cheapest.  
-  **Higher floors and taller buildings** attract premium pricing, reflecting lifestyle preferences.  

---

##  Future Work  

- Incorporate external datasets (e.g., infrastructure projects, public transport access).  
- Build predictive models for price forecasting.  
- Develop an interactive dashboard.  
- Automate data ingestion for regular market updates.  

---

##  Acknowledgments  

- Python libraries: Pandas, NumPy, Matplotlib.  
- Open-source learning resources that guided data cleaning and EDA.  

---

##  Contact  

Created by **Chinmay Mane**  
- GitHub: https://github.com/Chinmay3548 
- LinkedIn: https://www.linkedin.com/in/chinmay-mane-77389a20b/

---
