# Online Retail Sales Analysis

# *A Data Analytics Portfolio Project | Python · Pandas · Jupyter Notebook*

## Project Overview

This project explores transactional data from an online retail business between December 2010 and December 2011. The dataset was obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail).

Using Python and its data analysis libraries, this project examines sales performance, product trends, customer purchasing behavior, and geographic distribution. The work is organized into eight Jupyter notebooks covering data inspection, cleaning, and exploratory data analysis (EDA).

## Project Objectives

The objectives of this project are to:

- Inspect and prepare the original transactional dataset for analysis.
- Examine monthly revenue trends. 
- Identify products with the highest revenue and sales quantity.
- Explore monthly product performance.
- Identify customers with high revenue, purchase quantity, and order frequency.
- Compare sales performance across countries.

## Dataset

- **Dataset:** Online Retail
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Creators:** Daqing Chen, Sai Laing Sain, Kun Guo
- **Time period:** December 2010 – December 2011
- **License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
- **DOI:** [10.24432/C5BW33](https://doi.org/10.24432/C5BW33)

The original dataset contains 541,909 transaction records and eight columns.

## Tools and Technologies

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

retail-online-analysis/
├── data/
│   ├── Online Retail.xlsx
│   ├── product_sales.csv
│   └── sales_data_deduped.csv
├── notebooks/
│   ├── 01_data_inspection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_monthly_revenue_analysis.ipynb
│   ├── 04_description_analysis.ipynb
│   ├── 05_product_analysis.ipynb
│   ├── 06_monthly_product_analysis.ipynb
│   ├── 07_customer_analysis.ipynb
│   └── 08_geographic_analysis.ipynb
├── pictures/
│   ├── 03_monthly_revenue_line_graph.png
│   ├── 05_best_selling_products_by_quantity.png
│   ├── 05_best_selling_products_by_revenue.png
│   ├── 06_monthly_best_selling_products_by_quantity.png
│   ├── 06_monthly_best_selling_products_by_revenue.png
│   ├── 07_top_ten_customers_by_order_count.png
│   ├── 07_top_ten_customers_by_quantity.png
│   ├── 07_top_ten_customers_by_revenue.png
│   ├── 08_top_ten_countries_by_order_count.png
│   ├── 08_top_ten_countries_by_quantity.png
│   ├── 08_top_ten_countries_by_revenue.png
│   ├── 08_top_ten_non_uk_countries_by_order_count.png
│   ├── 08_top_ten_non_uk_countries_by_quantity.png
│   └── 08_top_ten_non_uk_countries_by_revenue.png
└── README.md


## Analysis and Key Findings

### Notebook 01: Data Inspection

The initial inspection revealed:

- Dataset dimensions: 541,909 rows and 8 columns.
- Missing values: 1,454 in `Description` and 135,080 in `CustomerID`.
- Duplicate records: 5,268 rows.
- Negative quantities: 10,624 rows.
- Non-positive unit prices: 2,517 rows.
- Cancellation records: 9,288 rows with invoice numbers beginning with `C`.

### Notebook 02: Data Cleaning

The cleaning process involved:

- Filtering out cancellation records, negative quantities, and non-positive unit prices. There were no zero-quantity records.
- Removing exact duplicate rows.
- Exporting the resulting dataset as `sales_data_deduped.csv`.

The dataset was reduced from 541,909 to 524,878 rows.

### Notebook 03: Monthly Revenue Analysis

Using `sales_data_deduped.csv`, the analysis found:

- Total revenue across the thirteen months: **£10,642,110.80**.
- Highest-revenue month: **November 2011**, with **£1,503,866.78**.
- Lowest-revenue month: **February 2011**, with **£522,545.56**.

### Notebook 04: Description Analysis

Product descriptions were examined to identify records that did not represent physical merchandise, including postage charges, fees, manual adjustments, samples, and gift vouchers. These records were excluded to create a merchandise-focused dataset, saved as `product_sales.csv`.

The dataset was reduced from 524,878 to 522,692 rows.

### Notebook 05: Product Analysis

Using `product_sales.csv`, the analysis found:

- Highest-revenue product: **REGENCY CAKESTAND 3 TIER**, generating **£174,156.54**.
- Highest-quantity product: **PAPER CRAFT , LITTLE BIRDIE**, with **80,995 units** sold.

### Notebook 06: Monthly Product Analysis

This analysis examined the highest-performing product by revenue and quantity for each month.

In December 2011, **PAPER CRAFT , LITTLE BIRDIE** recorded the highest monthly product revenue (**£168,469.60**) and the highest monthly quantity (**80,995 units**) across the period.

### Notebook 07: Customer Analysis

Using `sales_data_deduped.csv`, the customer analysis identified:

- Highest total revenue among the top ten customers: **Customer 14646**, with **£280,206.02**.
- Highest total quantity among the top ten customers: **Customer 14646**, with **196,915 units**.
- Highest order count among the top ten customers: **Customer 12748**, with **209 orders**.

### Notebook 08: Geographic Analysis

The geographic analysis found:

- **United Kingdom:** Highest total revenue (**£8,726,000.34**), quantity sold (**4,639,155 units**), and order count (**17,912 orders**).
- **Outside the United Kingdom:** The **Netherlands** had the highest total revenue (**£283,889**) and quantity sold (**200,258 units**), while **Germany** had the highest order count (**443 orders**).

## Conclusion

This project provided an opportunity to apply Python and its libraries to a real-world transactional dataset and explore sales performance from several perspectives. The analysis covered overall revenue, product performance, customer purchasing behavior, and geographic distribution.

The findings show that the United Kingdom accounted for the largest share of the recorded sales activity, while individual products and customers contributed differently across the period. The project also provided practical experience in inspecting, cleaning, analyzing, and communicating insights from data.

## Acknowledgment

The Online Retail dataset was created by **Daqing Chen, Sai Laing Sain, Kun Guo** and is provided by the UCI Machine Learning Repository under the **CC BY 4.0** license. Please refer to the [dataset page](https://archive.ics.uci.edu/dataset/352/online+retail) and [license](https://creativecommons.org/licenses/by/4.0/) for the original source and terms of use.
