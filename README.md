## **House Price Analysis in Bangalore**

## **Introduction & Goal of the Project**
The goal of this project is to analyze house prices in Bangalore, focusing on price per square foot to detect and remove outliers. The key objectives include:

- Performing Exploratory Data Analysis (EDA)
- Detecting and removing outliers using different methods
- Visualizing the data using boxplots, histograms, scatter plots, and heatmaps
- Checking correlation between numerical features

## **Data Story & Preprocessing**
The dataset contains the following columns:

location – Area of the property
size – Number of bedrooms (BHK/Bedroom)
total_sqft – Total area of the house
bath – Number of bathrooms
price – Price of the property
bhk – Converted from 'size' column (BHK & Bedroom)
price_per_sqft – Price per square foot (computed as price/total_sqft)

## **Conclusion of the Analysis**  

### **Summary of Findings**  
1. **Basic EDA (Exploratory Data Analysis)**  
   - The dataset contained **property price data in Bangalore**, including key features like `total_sqft`, `bhk`, `bath`, `price`, and `price_per_sqft`.
   - Some inconsistencies in `bhk` and `bedroom` were cleaned.
   - The `price_per_sqft` column showed high variance and required outlier detection.

2. **Outlier Detection & Removal**  
   - Multiple methods were used:
     - **Mean & Standard Deviation**: Detected extreme values but didn't effectively remove all outliers.
     - **Percentile Method**: Removed values below **5th percentile** and above **95th percentile**.
     - **IQR (Interquartile Range)**: Best suited for removing extreme values effectively.
     - **Z-Score Method**: Performed well but required fine-tuning for thresholds.  
   - **Boxplots showed that IQR was the most effective method** for this dataset.

3. **Price per Sqft Distribution & Transformations**  
   - **Before transformation**: The distribution was **right-skewed**, meaning extreme high values were present.
   - **After log transformation**: The distribution became more normal with skewness reduced from **0.97 to -0.10**.
   - Kurtosis also improved, indicating a more uniform spread.

4. **Correlation Analysis**  
   - **Heatmap & Scatter Plots** revealed:
     - **Strong correlation between `total_sqft` and `price`** (expected).
     - **`bhk` and `bath` were highly correlated**, suggesting more bedrooms mean more bathrooms.
     - **`price_per_sqft` showed weak correlation** with other numerical variables, indicating that factors like location might play a crucial role.

5. **Scatter Plots for Correlation**  
   - Showed linear relationships between some features (e.g., **`total_sqft` vs. `price`**).
   - Some plots had **scattered points** (e.g., **`bhk` vs. `price_per_sqft`**), indicating weak or no correlation.

---

### **Final Insights & Recommendations**  
 **Key Takeaways:**
- Outlier detection was necessary as extreme values distorted the analysis.
- **IQR method was the most effective** in handling outliers.
- **Log transformation improved the distribution** of price per square foot.
