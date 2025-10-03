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

# 🔍 Analysis (Queries, Output, Insight, Recommendation)
## 🔹 Product Popularity & Customer Behavior

**Questions:**
1. Which products have the highest number of reviews?
2. Is there a correlation between product rating and total reviews?
3. Do higher-rated products lead to more sales last month?

---

## 1️⃣ Which products have the highest number of reviews?

### SQL Query
```sql
SELECT
    product_title,
    product_category,
    total_reviews,
    product_rating
FROM products
WHERE total_reviews IS NOT NULL
ORDER BY total_reviews DESC
LIMIT 10;

| Product Title | Category | Total Reviews | Rating |
|---------------|----------|---------------|--------|
| Amazon Basics 48-Pack AA Alkaline High-Performance Batteries, 1.5 Volt, 10-Year Shelf Life | Laptops | 865,598 | 4.7 |
| SanDisk 32GB Ultra microSDHC UHS-I Memory Card with Adapter - 98MB/s, C10, U1, Full HD, A1, Micro SD Card - SDSQUAR-032G-GN6MA | Chargers & Cables | 645,418 | 4.7 |
| [Older Version] SanDisk 32GB 2-Pack Ultra MicroSDHC UHS-I Memory Card (2x32GB) - SDSQUAR-032G-GN6MT | Storage | 645,416 | 4.7 |
| Amazon Basics AAA Alkaline High-Performance Batteries, 1.5 Volt, 10-Year Shelf Life, 36 Count (Pack of 1) | Laptops | 625,776 | 4.7 |
| Amazon Basics HDMI Cable, 3ft, 4K@60Hz, High-Speed 4K HDMI 2.0 Cord (18Gbps), 2160p, 48 bit, Compatible with TV/PS5/Xbox/Roku, Black | Chargers & Cables | 553,927 | 4.7 |
| Amazon Fire TV Stick, sharp picture quality, fast streaming, free & live TV, Alexa Voice Remote with TV controls | Smart Home | 517,617 | 4.7 |
| SanDisk 1TB Extreme microSDXC UHS-I Memory Card with Adapter - Up to 160MB/s, C10, U3, V30, 4K, A2, Micro SD - SDSQXA1-1T00-GN6MA | Chargers & Cables | 353,306 | 4.8 |
| [Older Version] SanDisk 128GB Ultra microSDXC UHS-I Memory Card with Adapter - 120MB/s, C10, U1, Full HD, A1, Micro SD Card - SDSQUA4-128G-GN6MA | Chargers & Cables | 315,834 | 4.7 |
| Blink Mini - Compact indoor plug-in smart security camera, 1080p HD video, night vision, motion detection, two-way audio, easy set up, Works with Alexa – 1 camera (Black) | Cameras | 302,790 | 4.4 |
| SanDisk Cruzer Blade 8GB USB 2.0 Flash Drive- SDCZ50-008G-B35 | Storage | 298,061 | 4.6 |


