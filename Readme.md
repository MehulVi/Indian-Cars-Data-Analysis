# Indian Car Market Analysis (Python)

An exploratory data analysis (EDA) project on the Indian car market. It looks at ex-showroom prices, brand categories, fuel types and transmission types across makes, using Python, with Excel used for the initial understanding of the data.

## Table of Contents

- [Project Overview](#project-overview)
- [Business Questions](#business-questions)
- [Dataset](#dataset)
- [Tools and Libraries](#tools-and-libraries)
- [Project Workflow](#project-workflow)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Project Structure](#project-structure)
- [Author](#author)

## Project Overview

The Indian car market has hundreds of models and variants across different price segments, fuel types and transmissions. This project analyses a dataset of Indian cars to understand:

- How prices differ across brands and categories
- Which brands offer Petrol, Diesel, CNG or Electric variants
- Which brands offer Manual, AMT or Automatic transmissions

> **Note:** The dataset contains specifications and pricing for each variant. It does not contain units sold. In this project, **Count** means the *number of variants* of a make or category, not sales volume.

## Business Questions

1. Which car brands have the highest total ex-showroom value in the market?
2. How is the market split across Budget, Mid-Range, Premium and Luxury categories?
3. Which brands offer Petrol and CNG variants?
4. Which brands offer Manual, AMT or Automatic transmissions?

## Dataset

| Item | Details |
|---|---|
| Format | CSV |
| Raw file | `Data/Raw_data/Indian_car_Raw_data.csv` |
| Cleaned file | `Data/Cleaned_data/Indian_car_Cleaned_data.csv` |

**Main columns used:**

| Column | Description |
|---|---|
| `Make` | Car brand (Hyundai, Tata, BMW, etc.) |
| `Model` / `Variant` | Car model and its variant |
| `EX- Showroom Price` | Ex-showroom price in rupees |
| `Ex- Showroom (Lakhs)` | Ex-showroom price in lakhs (renamed from `Column1`) |
| `Fuel_Type` | Petrol, Diesel, CNG, etc. |
| `Type` | Transmission type (Manual, AMT, Automatic) |
| `Category` | Budget, Mid-Range, Premium or Luxury |
| `Displacement`, `Cylinders`, `Power`, `Torque`, `Seating` | Engine and body specifications |

## Tools and Libraries

- **Python 3**: main language for analysis
- **Pandas**: data loading, cleaning and grouping
- **NumPy**: numerical operations
- **Matplotlib**: bar charts
- **Seaborn**: heatmaps
- **Microsoft Excel**: used to explore and understand the data (columns, filters, price ranges and units) before starting the analysis in Python
- **VS Code**: development environment
- **Git and GitHub**: version control

## Project Workflow

1. **Understanding the data in Excel.** Opened the raw file in Excel, applied filters, checked the columns, price values and units, and identified problems such as unclear column names.
2. **Data cleaning.** Checked and removed duplicates and missing values, and renamed `Column1` to `Ex- Showroom (Lakhs)`.
3. **Loading data in Python.** Loaded the cleaned CSV with Pandas and inspected the shape, data types and missing values.
4. **Analysis.**
   - Grouped by `Make` to get the variant count and total ex-showroom price
   - Grouped by `Category` to compare total price across segments
   - Built cross-tabulations of Make vs Fuel Type and Make vs Transmission Type
5. **Visualization.** Created bar charts and heatmaps, and saved them in the `images/` folder.
6. **Insights.** Summarised the findings below.

## Key Findings

- **Mercedes-Benz** has the highest total ex-showroom value (about Rs 115.6 Cr across 75 variants), largely because it has many variants in the dataset.
- **Lamborghini** (13 variants) and **Bugatti** (only 2 variants) rank high on total value despite having few variants, which shows very high prices per variant.
- By category, **Luxury** accounts for the largest total value (about Rs 452.6 Cr), followed by Mid-Range (about Rs 66.4 Cr), Premium (about Rs 44.3 Cr) and Budget (about Rs 23.2 Cr).
- The Make vs Fuel Type heatmap shows which brands offer Petrol, Diesel and CNG variants.
- The Make vs Transmission heatmap shows which brands offer Manual, AMT and Automatic variants.

> A total depends on the number of variants, so a high total does not always mean a more expensive brand. Average price per variant is a fairer comparison and is listed under future improvements.

## Visualizations

### Total Ex-Showroom Price by Make
![Total price by make](C:\Users\niraj\OneDrive\Desktop\python project\Indian cars datasets\notebook\images\make_total_simple.png)

### Total Price and Variant Count by Make
![Total price and count by make](C:\Users\niraj\OneDrive\Desktop\python project\Indian cars datasets\notebook\images\make_total_and_count.png)

### Total Ex-Showroom Price by Category
![Total price by category](C:\Users\niraj\OneDrive\Desktop\python project\Indian cars datasets\notebook\images\category_total_price.png)

### Variants by Make and Fuel Type
![Fuel type heatmap](C:\Users\niraj\OneDrive\Desktop\python project\Indian cars datasets\notebook\images\fuel_heatmap_table.png)

### Variants by Make and Transmission Type
![Transmission heatmap](C:\Users\niraj\OneDrive\Desktop\python project\Indian cars datasets\notebook\images\type_by_make.png)

## Project Structure

```
indian-car-analysis/
│
├── Data/
│   ├── Raw_data/
│   │   └── Indian_car_Raw_data.csv
│   └── Cleaned_data/
│       └── Indian_car_Cleaned_data.csv
│
├── images/                  # saved charts
├── main.py                  # full analysis script
├── requirements.txt         # Python libraries needed
├── .gitignore
└── README.md
```

## Author

**Your Name**
- GitHub: [Github](https://github.com/MehulVi)
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/mehul-vishwakarma-9a1b2431a/)

If you found this project useful, consider giving it a star.