# 🛒 E-Commerce Order Fulfillment Efficiency Analysis

An end-to-end **Data Analytics project** using the Olist Brazilian E-Commerce dataset to analyze **order fulfillment performance**, identify **delivery bottlenecks, high-risk states and sellers, and slow-performing product categories**, evaluate **delivery-estimate accuracy**, and measure how **late deliveries relate to customer ratings** through Python, SQL, statistical analysis, and Power BI.


## 📌 Overview

A data analytics project using the **Olist Brazilian E-Commerce Public Dataset** to evaluate order fulfillment performance, identify operational bottlenecks, and examine the relationship between delivery performance and customer satisfaction.

The analysis combines **Python, SQL, statistical validation, and Power BI** to move from raw order data to measurable operational insights.

---

## 🎯 Business Problem

E-commerce performance depends on more than simply completing an order. Delays can occur during payment approval, seller handoff, carrier transportation, and last-mile delivery.

This analysis answers:

- Where are fulfillment delays concentrated?
- Which states and product categories perform worst?
- Which sellers present higher operational risk?
- How does delivery performance vary over time?
- How accurate are promised delivery estimates?
- Which fulfillment stage has the strongest relationship with total delivery time?
- Is delivery performance associated with customer ratings?

---

## 📊 Dataset

**Source:** Olist Brazilian E-Commerce Public Dataset  
**Period:** 2017–2018

| Dataset | Records |
|---|---:|
| Orders | 96,315 |
| Order Items | 112,650 |
| Products | 32,951 |
| Sellers | 3,095 |
| Customers | 99,441 |

After data validation, **161 records with impossible negative shipping durations were removed**, retaining **99.83%** of the dataset.

---

## 🔎 Key Metrics

| KPI | Result |
|---|---:|
| On-Time Delivery Rate | **91.9%** |
| Late Orders | **7,827 (8.1%)** |
| Average Delivery Time | **12.57 days** |
| Median Delivery Time | **10.22 days** |
| Average Shipping Time | **3.24 days** |
| Average Approval Delay | **0.43 days** |
| Average Delivery Estimate Buffer | **12.3 days early** |

---

## 💡 Key Findings

### 1. Last-mile delivery is the dominant bottleneck

**Last-mile days vs. total delivery time: r = 0.928**

Shipping time had a much weaker relationship:

- Shipping → Delivery: **r = 0.402**
- Approval delay → Delivery: **r = 0.080**
- Last-mile → Delivery: **r = 0.928**

**Finding:** Last-mile performance has the strongest observed association with total fulfillment time.

---

### 2. Amazonas has the slowest average delivery

| State | Avg. Delivery |
|---|---:|
| Amazonas (AM) | **26.43 days** |
| Alagoas (AL) | 24.54 days |
| Pará (PA) | 23.78 days |
| Maranhão (MA) | 21.61 days |
| Sergipe (SE) | 21.55 days |

The gap between the slowest state and the 15th-slowest state was approximately **10.6 days**.

---

### 3. Office furniture is the slowest category

**Office Furniture**

- Average delivery: **20.84 days**
- Average last-mile: **9.98 days**
- Last-mile share: **48%**
- Late rate: **8.93%**
- Average seller handoff: **10.87 days**

National average last-mile time: **9.33 days**

---

### 4. March 2018 had the weakest delivery performance

| Month | On-Time | Late |
|---|---:|---:|
| February 2018 | 84.00% | 16.00% |
| **March 2018** | **78.64%** | **21.36%** |
| April 2018 | 94.68% | 5.32% |
| June 2018 | **98.65%** | **1.35%** |

**March 2018 recorded the lowest on-time delivery rate at 78.64%.**

---

### 5. A small group of sellers showed high delivery risk

**15 sellers** recorded late-delivery rates above **25%**.

Together they handled:

- **792 orders**
- **243 late deliveries**

This identifies a concentrated group for operational review.

---

### 6. Delivery estimates contained a large buffer

Average delivery deviation was:

**−12.30 days**

Orders were delivered approximately **12.3 days earlier than the estimated delivery date on average**.

This indicates substantial estimation buffer in the observed data.

---

### 7. Late delivery strongly differed from customer ratings

| Group | Avg. Review Score |
|---|---:|
| On-Time Orders | **4.29** |
| Late Orders | **2.27** |
| Difference | **2.02 points** |

An independent two-sample t-test produced:

- **t-statistic:** −132.0713
- **p-value:** < 0.0001
- **α:** 0.05
- **Decision:** Reject H₀

**Finding:** The difference in review scores between late and on-time orders was statistically significant.

---

## 📈 Power BI Dashboard

The Power BI dashboard brings the operational findings into a decision-oriented view.

**Key KPIs:**

- **91.9%** On-Time Delivery Rate
- **12.6 days** Average Fulfillment Time
- **3.2 days** Average Carrier Handoff Time
- **7,827** Late Orders
- **−12.3 days** Estimation Buffer

![Olist E-Commerce Performance Dashboard](https://github.com/Hanne-Jenifer/Ecommerce_Order_Fulfillment_Analysis/blob/419e4a86bc7956a634057a213a6fd6b320ad3579/Task3_Deep-Dive%20Analysis%20%26%20Interactive%20Dashboarding/Olist%20E-Commerce%20Performance%20Dashboard.png)

![Sales Overview](https://github.com/Hanne-Jenifer/Ecommerce_Order_Fulfillment_Analysis/blob/419e4a86bc7956a634057a213a6fd6b320ad3579/Task3_Deep-Dive%20Analysis%20%26%20Interactive%20Dashboarding/Sales%20Overview.png)

![Customer and Seller Analysis](https://github.com/Hanne-Jenifer/Ecommerce_Order_Fulfillment_Analysis/blob/419e4a86bc7956a634057a213a6fd6b320ad3579/Task3_Deep-Dive%20Analysis%20%26%20Interactive%20Dashboarding/Customer%20Analysis.png)

![Order Performance Analysis](https://github.com/Hanne-Jenifer/Ecommerce_Order_Fulfillment_Analysis/blob/419e4a86bc7956a634057a213a6fd6b320ad3579/Task3_Deep-Dive%20Analysis%20%26%20Interactive%20Dashboarding/Order%20Performance%20Analysis.png)

---

## 🧭 Business Actions

Based on the analysis:

1. **Prioritize last-mile performance** as the primary fulfillment improvement area.
2. **Investigate high-risk sellers** with consistently high late-delivery rates.
3. **Review regional logistics performance**, particularly slower states such as Amazonas and Alagoas.
4. **Reassess delivery estimates** to reduce excessive estimation buffers.
5. **Monitor categories with longer fulfillment cycles**, especially Office Furniture.

---

## 🛠️ Tools & Technologies

- **Python** — Data cleaning, analysis, statistical testing
- **Pandas / NumPy** — Data manipulation
- **Matplotlib / Seaborn** — Exploratory visualization
- **SQL / SQLite** — Business-focused analysis
- **SciPy** — Statistical validation
- **Power BI** — Interactive dashboarding

---

## 📌 Project Outcome

The analysis identified **last-mile delivery as the strongest fulfillment bottleneck**, highlighted significant geographic and category-level performance gaps, isolated **15 high-risk sellers**, exposed a **12.3-day estimation buffer**, and demonstrated a **2.02-point difference in average customer ratings** between late and on-time orders.

The findings were translated into a **Power BI dashboard** for operational monitoring and decision-making.

---

## 👤 Author

**Hanne Jenifer**
