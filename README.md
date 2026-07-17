# Amazon Product Review Analysis

## Screenshots

---

### Amazon Product Review Analysis
![Amazon Product Review Analysis](https://github.com/parthadata7/Amazon-Customer-Review-Analytics-Dashboard/blob/main/screenshots/dashboard.PNG)

---

## Project Overview

This project analyzes 30,839 customer reviews for a single Amazon product sold by 21 different sellers between October 2014 and August 2015. The goal is to uncover customer satisfaction trends, seller performance, and the key drivers behind negative reviews to support data-driven business decisions.

---

# 🎯 Business Questions

* What is the overall level of customer satisfaction?
* Which sellers perform the best and worst based on ratings and reviews?
* How does review activity change over time?
* What is the overall customer sentiment?
* What are the most common customer complaints?
* What actions can improve customer satisfaction and seller performance?

---

## Objectives

- Clean and prepare raw review data for analysis.
- Perform exploratory data analysis (EDA) to identify trends across sellers and time.
- Conduct sentiment analysis to quantify positive vs. negative feedback.
- Categorize customer complaints to pinpoint recurring issues.
- Translate findings into actionable business recommendations.

---

## Dataset Description

- customer_id
- product_id
- product_title
- star_rating
- helpful_votes
- total_votes
- verified_purchase
- review_date
- review_headline
- review_Body
- seller_id
- sentiment_label

---

## Tech Stack

| Tool             | Purpose                                 |
| ---------------- | --------------------------------------- |
| Python (Pandas)  |  data cleaning, analysis, and sentiment/complaint categorization |
| Microsoft Excel  | Interactive dashboard and visualization |
| Jupyter Notebook | Analysis environment                    |


---

## Project Workflow

1. **Data Understanding & Cleaning** – Inspected dataset structure, handled missing values, standardized fields.
2. **Exploratory Data Analysis** – Analyzed rating distributions, seller performance, and monthly review trends.
3. **Sentiment Analysis** – Classified reviews as positive/negative and identified sentiment drivers.
4. **Complaint Categorization** – Grouped negative reviews into issue categories (app, device, battery, etc.).
5. **Dashboard Design (Excel)** – Built an interactive dashboard to visualize key metrics and trends.
6. **Insights & Recommendations** – Compiled findings into a business-ready summary.

---

## 📈 Dashboard Features

* Displays key KPIs: Total Reviews, Positive Reviews, Negative Reviews, Average Rating, and Verified Purchases.
* Shows review and rating trends over time.
* Visualizes rating and sentiment distribution.
* Compares verified vs. unverified customer reviews.
* Highlights top sellers by review volume and average rating.
* Compares positive and negative review percentages across sellers.


---

## 📐 DAX Measures Used

| Measure Name                 | DAX Formula                                                                                                      | Description                                    |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| **positive_review**          | `DAX<br>positive_review = CALCULATE( COUNT(Range[sentiment_label]), Range[sentiment_label] = "POSITIVE" )`       | Counts the total number of positive reviews.   |
| **negative_review**          | `DAX<br>negative_review = CALCULATE( COUNT(Range[sentiment_label]), Range[sentiment_label] = "NEGATIVE" )`       | Counts the total number of negative reviews.   |
| **no_of_verified_purchases** | `DAX<br>no_of_verified_purchases = CALCULATE( COUNT(Range[verified_purchase]), Range[verified_purchase] = "Y" )` | Counts the total number of verified purchases. |
| **no_of_neutral**            | `DAX<br>no_of_neutral = CALCULATE( COUNT(Range[sentiment_label]), Range[sentiment_label] = "Neutral" )`          | Counts the total number of neutral reviews.    |

---

## 🧠 Key Insights

* Customer satisfaction is high with an **average rating of 4.34**.
* **84% of reviews are positive**, indicating a strong customer experience.
* **87% of reviews are from verified purchasers**.
* **Seller_3** has the highest review volume but also requires performance improvement.
* **Seller_13** is the best-performing seller based on average rating.
* Review activity peaked in **January 2015**, showing the highest customer engagement.

---

# 📊 Pandas Data Analysis

---

## Sentiment Analysis

###positive vs. negative vs. neutral reviews

![positive vs. negative vs. neutral reviews](https://github.com/parthadata7/Amazon-Customer-Review-Analytics-Dashboard/blob/main/screenshots/charts/3a.png)

### Insights

- **83.54%** of reviews are positive, reinforcing strong overall customer satisfaction.
- Only **9.28%** of reviews are negative.

---

###Rating Distribution

![Rating Distribution](https://github.com/parthadata7/Amazon-Customer-Review-Analytics-Dashboard/blob/main/screenshots/charts/3b.png)

### Insights

- Five-star ratings dominate customer feedback.

---

###Word Cloud : Positive vs Negative

![Word Cloud](https://github.com/parthadata7/Amazon-Customer-Review-Analytics-Dashboard/blob/main/screenshots/charts/3c.png)

### Insights

- Positive sentiment is tied to product usability and overall experience; negative sentiment centers on device functionality, apps, and screen issues.

---

## Customer Complaint Categorization

###Complaint Categories

![Complaint Categories](https://github.com/parthadata7/Amazon-Customer-Review-Analytics-Dashboard/blob/main/screenshots/charts/4a.png)

### Insights

- **App Issues** are the leading complaint category, making up over a third of all negative feedback.
- **App + Device Performance + Battery** issues together account for **over 56%** of negative reviews, pointing to software and hardware reliability as the top priorities.
- Logistics-related issues (delivery, price, packaging, durability) are minor by comparison.
- Improving software performance would address most customer dissatisfaction.

---

## Insights & Recommendations

### Key Insights

* Customer satisfaction is high, with an average rating of **4.33** and **83.5% positive reviews**.
* **Seller_3** generated the highest review volume (39% of all reviews) but also recorded the highest number of negative reviews.
* **Seller_13** is the top performer, with the highest average rating (4.52) across 1,755 reviews.
* Review activity and satisfaction both peaked in January 2015 (8,015 reviews; rating rose from 4.08 to 4.42 since Nov 2014).
* **App Issues** are the leading complaint category (36.84% of negative reviews), followed by **Device Performance** (11.39%) and **Battery Issues** (8.32%).


**Recommendations**
- **Prioritize app improvements** – Fix crashes, bugs, and usability issues to address 1,000+ complaints.
- **Investigate Seller_3** – Review product quality and support practices to reduce its outsized share of negative feedback.
- **Benchmark against Seller_13** – Apply its practices as a quality/service standard for other sellers.
- **Improve product reliability** – Focus on device performance and battery optimization (564 combined complaints).
- **Strengthen delivery operations** – Improve shipping communication and tracking to fix the most severe dissatisfaction driver.

---

# 🎯 Executive Summary

Analysis of **30,839 customer reviews** across **21 sellers** shows strong overall customer satisfaction, with an average rating of **4.33** and **83.5% positive reviews**. While Seller_3 drives the majority of customer engagement, it also contributes the highest number of negative reviews, indicating an opportunity for improvement. Seller_13 consistently delivers the best customer experience with the highest average rating. Complaint analysis reveals that app-related issues, device performance, and battery problems are the primary drivers of negative feedback. Addressing these areas can significantly improve customer satisfaction and seller performance.


---

## Conclusion

This project demonstrates how data analytics can transform customer review data into actionable business insights. Through data cleaning, exploratory analysis, sentiment analysis, and complaint categorization, the project identifies high-performing sellers, highlights improvement opportunities, and provides practical recommendations that can enhance customer satisfaction and support data-driven business decisions.


---

## Project Structure

```text
├── data/
│   ├──customer_reviews.xlsx
│   └──dashboard.xlsx
├── screenshots/
│   ├──assets
│   ├──charts
│   ├──dashboard.png
├── Python(panda)
└── README.md
```

---

## Contact

**Name:** Partha Pratim Das

**Email:** [parthadataanalyst@gmail.com](mailto:parthadataanalyst@gmail.com)

**LinkedIn:** []()

**Portfolio:** []()

**GitHub:** []()
