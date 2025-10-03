# Exploratory Data Analysis on Amazon Dataset

## Project Overview

This project conducts exploratory data analysis (EDA) on an Amazon dataset consisting of product and review information. The notebook (`EDA_AMAZON-checkpoint.ipynb`) explores data distribution, cleans values, and visualizes relationships between product attributes such as prices, ratings, and discounts.

---

## Dataset Information

* **Number of rows:** 1465
* **Number of columns:** 16

### Columns

* `product_id`
* `product_name`
* `category`
* `discounted_price`
* `actual_price`
* `discount_percentage`
* `rating`
* `rating_count`
* `about_product`
* `user_id`
* `user_name`
* `review_id`
* `review_title`
* `review_content`
* `img_link`
* `product_link`

### Missing Values

Most columns have no missing values. Only `rating_count` has **2 missing values**.

---

## Sample Data

| product_id | product_name                                              | category                | discounted_price | actual_price | discount_percentage | rating | rating_count |
| ---------- | --------------------------------------------------------- | ----------------------- | ---------------- | ------------ | ------------------- | ------ | ------------ |
| B07JW9H4J1 | Wayona Nylon Braided USB to Lightning Fast Charging Cable | Computers & Accessories | ₹399             | ₹1,099       | 64%                 | 4.2    | 24,269       |
| B098NS6PVG | Ambrane Unbreakable 60W / 3A Fast Charging Cable          | Computers & Accessories | ₹199             | ₹349         | 43%                 | 4.0    | 43,994       |
| B096MSW6CT | Sounce Fast Phone Charging Cable                          | Computers & Accessories | ₹199             | ₹1,899       | 90%                 | 3.9    | 7,928        |
| B08HDJ86NZ | boAt Deuce USB 300 2 in 1 Type-C & Micro USB Cable        | Computers & Accessories | ₹329             | ₹699         | 53%                 | 4.2    | 94,363       |
| B08CF3B7N1 | Portronics Konnect L 1.2M Fast Charging Cable             | Computers & Accessories | ₹154             | ₹399         | 61%                 | 4.2    | 16,905       |

---

## Key Findings

### 1. Distribution of Ratings

* Ratings are mostly clustered between **3.5 and 4.5**.
* Indicates majority of products are rated positively.

### 2. Discounts and Pricing

* Large discounts (up to **90%**) are present in the dataset.
* Many products have a big gap between `actual_price` and `discounted_price`.

### 3. Correlations

* **Rating vs Discount Percentage** → Weak negative correlation (-0.15).
* **Discounted Price vs Rating** → Slight positive correlation (~0.12).
* Interpretation: Discounts do not strongly influence ratings.

### 4. Top Products (by rating_count)

* Products like **boAt charging cables** and **Ambrane cables** dominate the dataset with very high review counts (90k+ reviews).
* These appear as best-selling items.

---

## Visualizations

The notebook includes:

* Distribution plots of ratings, prices, and discounts.
* Correlation heatmaps.
* Price vs Rating scatter plots.
* Histograms of discount percentages.

---

## Dependencies

Install required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/eeshan15/Exploratory-Data-analysis-on-Amazon-Dataset.git
   ```
2. Open the notebook in Jupyter:

   ```bash
   jupyter notebook EDA_AMAZON-checkpoint.ipynb
   ```
3. Execute the cells in order.

---

## Insights Summary

* The dataset is clean with very few missing values.
* High-discount products are common but not always associated with higher ratings.
* Positive bias in ratings (most are 4+).
* A few popular products dominate the reviews, suggesting a skew towards bestsellers.

---

## License

This project is released under the MIT License.
