# 📊 Amazon Electronics Sales Analysis — SQL Portfolio Project
<p align="center">
  <img src="https://img.shields.io/badge/Language-SQL-blue?style=for-the-badge&logo=postgresql" />
  <img src="https://img.shields.io/badge/Tool-Data%20Analytics-green?style=for-the-badge&logo=databricks" />
  <img src="https://img.shields.io/badge/Platform-GitHub-black?style=for-the-badge&logo=github" />
</p>

## 📌 Problem Statement  

The primary objective of this project is to analyze **Amazon Electronics Product Sales** (42K+ items, 17 features) in order to uncover trends, customer preferences, and product performance drivers.  

By leveraging **SQL**, this project explores how **discounts, ratings, reviews, Best Seller tags, sponsorships, coupons, BuyBox availability, delivery options, and sustainability tags** influence customer engagement and sales.  

This analysis aims to answer key **business questions** that can help sellers optimize **pricing, marketing, and inventory strategies** to maximize sales and customer satisfaction.  

## 📊 Dataset Overview  

This project uses the **Amazon Electronics Product Sales Dataset (2025)**, sourced from [Kaggle](https://www.kaggle.com/) 📂.  
The dataset contains **42,000+ electronics products** with **17 key features**, including sales, ratings, pricing, discounts, delivery, and sustainability tags.  

The cleaned dataset provides valuable information to analyze customer preferences, product performance, and market strategies.  

---

### 🗂️ Features Overview  
Below are the key columns included in the **cleaned dataset** (the raw/unprocessed version contains similar fields):  

- **`product_title`** – Complete name/title of the product  
- **`product_rating`** – Average customer rating (numeric) out of 5  
- **`total_reviews`** – Total number of customer reviews  
- **`purchased_last_month`** – Units purchased in the last month  
- **`discounted_price`** – Current price after discount  
- **`original_price`** – Original listed price before discount  
- **`discount_percentage`** – Percentage discount applied to the product  
- **`is_best_seller`** – Indicates if the product is tagged as a Best Seller  
- **`is_sponsored`** – Whether the product is a Sponsored item or Organic  
- **`has_coupon`** – Availability of special discounted coupons (True/False)  
- **`buy_box_availability`** – BuyBox button availability on Amazon search page (NaN = False)  
- **`delivery_date`** – Estimated delivery date (converted to datetime format)  
- **`sustainability_tags`** – Eco-friendly and sustainability-related tags  
- **`product_image_url`** – Direct image link of the product  
- **`product_page_url`** – Official Amazon product page URL  
- **`data_collected_at`** – Date when the data was collected  
- **`product_category`** – Assigned product category based on the product title  

---

