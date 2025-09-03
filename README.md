# Data Cleaning & Insights Generation on Surat's Housing Dataset
This project focuses on cleaning and analyzing a housing dataset from Surat, India to derive meaningful insights for potential buyers, sellers, and real estate stakeholders. The raw dataset contained inconsistencies, missing values, and outliers, which were systematically cleaned using Python. Once cleaned, the dataset was explored to uncover meaningful patterns and trends in Surat’s real estate market, including property type distributions, location-based pricing, and the relationship between property size and price per square foot. 

The raw dataset contained multiple inconsistencies, missing values, and unrealistic entries that needed to be addressed before meaningful analysis. The following cleaning steps were performed:

### 1. Handled missing values 

   * Identified columns with null or incomplete data.

   * Removed rows with too many missing fields.

   * Kept missing rows in 'description' column since they had other relevant data for further analysis.

   * Imputed numerical missing values where it was possible, removed the rest.

### 2. Handled duplicates

* Checked for and removed duplicate property listings to avoid skewed results.


### 3. Converted data types

* In the original dataset, all the columns data type were object. These were handled by converting the columns to their relevant data types.

### 4. Created new columns

* The floors column was in 'x out of y' format. Converted this to two columns of x and y. This is helpful for statistical modelling.

* There is a price column which is easier to read (example: 84 lac). Another column called price_num was created which converted 84 lac to 8400000. Again, this is helpful for statistical modelling.

### 5. Handled outliers

* There was a lot of irrelevant information as outliers in the floor column. Those were removed.

* The price per sqft and price columns had some outliers too. Those were identified and dropped.

* furnishing columns had some outliers too. These were only a handful and were dropped.


## Insights

### Average price per square foot in Surat was found out to be RS. 4926.61

### Highest and lowest average price per sqft by locality were calculated.

### A correlation of 0.556 between square feet and price per square foot was observed auggesting a moderate positive relationship

* As the property size increases, the price per square foot also tends to increase.

* This indicates that larger properties are generally priced higher per sq. ft. compared to smaller ones.

* However, since the correlation is not very strong (not close to 1), there are exceptions—some large properties may still have lower price per sq. ft. due to location, demand, or age of construction.
