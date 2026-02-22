# Telco Strategic Retention Optimizer: Prescriptive Causal AI Suite
**Optimizing Marketing ROI through Uplift Modeling & Randomized Controlled Trials (A/B Testing)**

---

## 📌 Executive Summary: Solving the "Predictive Churn Paradox"
Standard churn models are mathematically inefficient because they target everyone likely to leave. This results in **"Marketing Cannibalization"**—offering expensive discounts to "Sure Things" who would have stayed anyway, and wasting budget on "Lost Causes" who leave regardless of the offer.

This project implements **Causal AI (Uplift Modeling)** to solve this paradox. By analyzing the results of a **20% Retention Discount Experiment**, I identified the **"Persuadable"** segment—the only group where a marketing intervention actually drives incremental revenue—uncovering a **$1.22M revenue recovery opportunity**.



---

## 🏗 Domain & Dataset Architecture
* **Industry Domain:** Telecommunications (Subscription-based Business Model).
* **Dataset Source:** Derived from the **IBM Sample Data (Telco Customer Churn)** via [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn), representing a home phone and internet services provider in California.
* **Project Scope:** While the original dataset is a static set of ~7k records, this project **upsampled the data to 100,000 records** to simulate enterprise-scale messy data. 

---

## 🚀 Key Business Impacts
* **Incremental Revenue Recovery:** Identified **$1.22M in Annual Recurring Revenue** by shifting to "Lift-based" targeting.
* **Efficiency Gain:** Radical surgical marketing precision by identifying the specific customer profile that responds to discounts.
* **Margin Protection:** Saved significant margin by identifying "Sure Things" who should remain at full price.

---

## 🔬 The Experimental Framework (A/B Test)
This project simulates a **Randomized Controlled Trial (RCT)**:
* **The Treatment:** A random 50% of the customer base was offered a **20% monthly discount** (The "Intervention").
* **The Control:** The remaining 50% received no offer.
* **The Goal:** Calculate the **Individual Treatment Effect (ITE)**—the delta in stay-probability caused *only* by the discount.

---

## 📊 Strategic Dashboard & Stakeholder Recommendations
**[🔗 View the Power BI Dashboard Here](https://app.powerbi.com/view?r=eyJrIjoiM2U0ZWFkYWEtYWQxZi00NTNmLWE0Y2UtMGFiZDk5MTc4ZGNmIiwidCI6IjExMTNiZTM0LWFlZDEtNGQwMC1hYjRiLWNkZDAyNTEwYmU5MSIsImMiOjN9)**

The Power BI Strategic Suite serves as the "Control Center" for the Marketing and Customer Success teams. It translates complex Causal AI outputs into three actionable views:

### 1. The Executive ROI Tracker (CFO/VP Level)
* **Feature:** Financial modeling of the $1.22M potential recovery.
* **Recommendation:** Shift the budget focus from "High-Risk Churn" to "High-Lift Persuadables." This allows for a **30% reduction in marketing spend** while maintaining identical retention KPIs.

### 2. The Segment Deep Dive (Marketing Ops Level)
* **Feature:** Breakdown of uplift by contract type and internet service.
* **Recommendation:** Focus 72% of retention campaign resources on **Fiber Optic customers on Month-to-Month contracts**. This group has the highest sensitivity to the 20% discount offer.

### 3. The Operational Call List (Customer Success Level)
* **Feature:** A dynamic, filterable table of customers ranked by their **Uplift Score**.
* **Recommendation:** CS agents should ignore "Lost Causes" (who consume high resource time with no retention ROI) and prioritize outreach to customers with an Uplift Score > 0.15.

---

## 🛠 Tech Stack & Methodology

This project utilizes a Causal Inference framework to transition from predictive churn modeling to prescriptive retention strategy.

### 1. Causal Inference & Uplift Modeling (Python/Scikit-Learn)
* **S-Learner Framework:** Implemented a Single-Learner (S-Learner) architecture using a **Random Forest Classifier**. By treating the retention offer as a binary feature (`is_treatment`), the model estimates the **Individual Treatment Effect (ITE)**.
* **Uplift Scoring:** Derived the uplift score by calculating the difference between the probability of staying when treated vs. the probability of staying in the control group:
$$\text{Uplift} = P(\text{Stay} | T=1) - P(\text{Stay} | T=0)$$
* **Behavioral Segmentation:** Automated decile-based categorization to isolate **'Persuadables'** from 'Sure Things' and 'Lost Causes,' mitigating marketing cannibalization.

### 2. Data Engineering Pipeline (Data Architecture & SQL)
* **Simulation at Scale:** Upsampled raw data to **100,000 records** to simulate production-level variance and ensure statistical significance in causal effects.
* **Feature Engineering:** Developed custom metrics including **Charge Velocity** (spend intensity) and engineered categorical features via One-Hot Encoding while maintaining data lineage through unique `customerID` hashes.
* **Validation:** Utilized a 20% holdout set to ensure the model generalizes to unseen data, preventing overfitting in the ROI projections.

### 3. Prescriptive Analytics (Power BI, DAX)
* **DAX Intelligence:** Developed complex measures using **iterator functions (`SUMX`)** to calculate annualized revenue impact at the individual customer level.
* **Visual Strategy:** Built a high-signal, minimalist UI focusing on **Behavioral Matrixes** and **Gains Charts** to identify high-elasticity cohorts.
* **Operational Execution:** Integrated a dynamic **Priority Call List** to bridge the gap between model inference and Customer Success outreach.

---

## 📂 Repository Structure
* `telco_uplift_dataset.csv`: The cleaned 100k record master dataset.
* `Customer_Retention.ipynb`: The end-to-end Python & SQL pipeline.
* `Customer Retention & Incremental Lift Optimizer.pbix`: The Power BI Strategic Suite.
* `Telco_Dataset.csv`: Final scored dataset used for the visualization.

---

## 👤 Contact
**Noopur Shekhar Divekar** | [LinkedIn Profile](https://www.linkedin.com/in/noopurd/) | [Email](mailto:noopur.div188@gmail.com)
