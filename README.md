# Amazon Data Analysis Project 📊

## Project Overview
This project performs a comprehensive analysis of Amazon product data to understand pricing strategies, customer engagement, and category-wise discount patterns. The analysis answers three critical business questions through data exploration, cleaning, and statistical visualization.

---

## 📋 Questions Analyzed

### **Q1: Do Higher Discounts Increase Sales?**
Analyzes the correlation between discount percentage and sales volume (measured by rating count)

### **Q2: Do People Look at Product Ratings?**
Investigates how product ratings influence customer engagement and reviews

### **Q3: Which Category Offers the Highest Discount?**
Identifies top 10 product categories with the highest average discount percentages

---

## 🛠️ Tools & Technologies Used

### **Programming Languages**
- **Python 3.x** - Core programming language for data analysis

### **Python Libraries**
| Library | Purpose |
|---------|---------|
| **Pandas** | Data manipulation, cleaning, and aggregation |
| **Matplotlib** | Static data visualization and chart creation |
| **Seaborn** | Statistical data visualization and styling |
| **Warnings** | Suppress non-critical warning messages |

### **Data Tools**
- **Jupyter Notebook** - Interactive analysis and documentation
- **CSV Format** - Data input/output
- **Power BI** - Business intelligence visualization (future integration)
- **R Language** - Statistical analysis (future integration)
- **Excel** - Data validation and reporting (future integration)

---

## 📁 Project Structure

```
amozon_service/
├── service.ipynb                    # Main analysis notebook
├── README.md                        # This file
├── REPORT.md                        # Detailed analysis report
├── Cell output 4 [DW].csv          # Generated output data
├── Cell output 5 [DW].csv          # Generated output data
├── Cell output 7 [DW].csv          # Generated output data
├── q1_discount_vs_sales.png        # Q1 scatter plot chart
├── q2_rating_vs_reviews.png        # Q2 bar chart
├── q3_category_discount.png        # Q3 horizontal bar chart
└── bonus_heatmap.png               # Correlation heatmap

Data Source: D:\archive (10)\amazon.csv
```

---

## 🔄 Analysis Workflow

### **Step 1: Data Loading**
- Load Amazon product dataset from CSV file
- Display basic information: rows, columns, first few records

### **Step 2: Data Exploration (EDA)**
- Examine column names and data types
- Check for missing values and duplicates
- Generate descriptive statistics

### **Step 3: Data Cleaning**
- Remove special characters (₹, %, commas) from price and percentage columns
- Convert text data to numeric format (float/int)
- Handle missing values and null entries
- Standardize category names into main categories
- **Data Quality**: Reduced from initial rows by dropping null values in key columns

### **Step 4a: Correlation Analysis (Q1)**
- Calculate Pearson correlation between discount percentage and rating count
- Generate scatter plot visualization
- Interpret correlation strength

### **Step 4b: Rating Bucketing Analysis (Q2)**
- Create rating buckets: [0-2], [2-3], [3-3.5], [3.5-4], [4-4.5], [4.5-5]
- Calculate average rating count per bucket
- Visualize with bar chart

### **Step 4c: Category Aggregation (Q3)**
- Group by main category and calculate mean discount percentage
- Rank categories by discount
- Display top 10 categories
- Create horizontal bar chart visualization

### **Step 5: Bonus Analysis**
- Generate correlation matrix across all key variables
- Create heatmap visualization
- Identify relationships between multiple factors

### **Step 6: Insights Summary**
- Compile findings and key takeaways
- Export all visualizations as PNG files

---

## 📊 Key Visualizations Generated

1. **q1_discount_vs_sales.png** - Scatter plot showing discount vs sales correlation
2. **q2_rating_vs_reviews.png** - Bar chart showing rating ranges vs average reviews
3. **q3_category_discount.png** - Top 10 categories by average discount (horizontal bar)
4. **bonus_heatmap.png** - Correlation matrix heatmap of all key variables

---

## 📈 Data Variables Analyzed

| Variable | Description |
|----------|-------------|
| `discount_percentage` | Product discount offered (%) |
| `actual_price` | Original product price (₹) |
| `discounted_price` | Final selling price after discount (₹) |
| `rating` | Customer rating (0-5 scale) |
| `rating_count` | Number of customer reviews (proxy for sales) |
| `category` | Product category (single or multi-level) |
| `main_category` | Standardized primary category |

---

## 🔧 Installation & Setup

### **Requirements**
```
pandas
matplotlib
seaborn
python >= 3.7
```

### **Install Dependencies**
```bash
pip install pandas matplotlib seaborn
```

### **Run Analysis**
1. Open Jupyter Notebook: `service.ipynb`
2. Update data path if needed: `D:\archive (10)\amazon.csv`
3. Execute cells sequentially (Cell 17 contains complete analysis)
4. Review generated PNG charts and outputs

---

## 📌 How to Use This Project

1. **For Quick Overview**: Read `REPORT.md`
2. **For Detailed Analysis**: Examine `service.ipynb` (Cell 17)
3. **For Visualizations**: Check generated PNG files
4. **For Data Exploration**: Use individual exploration cells

---

## 🎯 Future Enhancements

- [ ] Integrate Power BI dashboards for interactive exploration
- [ ] Add R language statistical tests
- [ ] Export summary tables to Excel
- [ ] Build predictive models for discount impact
- [ ] Create automated report generation
- [ ] Add time-series analysis for seasonal patterns

---

## 📝 Notes

- Missing values in key columns are dropped during cleaning (impact noted in final data shape)
- All prices are in Indian Rupees (₹)
- Rating count used as proxy for sales volume
- Analysis suppresses pandas/matplotlib warnings for cleaner output

---

## 👨‍💻 Author
Amazon Data Analysis Project | 2024

## 📄 License
Educational & Analytical Purpose

---

**Last Updated**: 2024 | **Analysis Status**: Complete ✅
