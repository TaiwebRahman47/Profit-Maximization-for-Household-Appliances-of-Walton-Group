# Profit Maximization for Walton Group Household Appliances Using Linear Programming

An Operations Research project focused on optimizing the product mix for **Walton Group**, Bangladesh's leading electronics and household appliance manufacturer, to maximize annual profit subject to production capacity, budget, and raw material constraints.

---

## 📌 Project Overview

Local manufacturing enterprises face complex decision-making challenges regarding resource allocation and production planning. This project utilizes **Linear Programming (LP)** and the **Simplex Method** to formulate and solve a product-mix optimization problem for Walton Group’s core household appliances.

### Key Objectives
- Model the annual profit maximization problem using empirical market and manufacturing data.
- Determine the optimal quantity to produce across primary appliance lines:
  - **Freezer & Refrigerator** ($X_1$)
  - **Air Conditioner** ($X_2$)
  - **Washing Machine** ($X_3$)
  - **Television** ($X_4$)
- Analyze capacity, raw material utilization, and budget bottlenecks.

---

## 📊 Dataset & Formulation Summary

### 1. Decision Variables
- $X_1$: Number of **Freezer & Refrigerator** units to produce per year
- $X_2$: Number of **Air Conditioner** units to produce per year
- $X_3$: Number of **Washing Machine** units to produce per year
- $X_4$: Number of **Television** units to produce per year

### 2. Financial Metrics per Unit

| Product Line | Avg. Selling Price (BDT) | Cost (BDT) | Profit Margin (BDT) |
| :--- | :---: | :---: | :---: |
| **Freezer & Refrigerator** | 37,269 | 20,850 | **16,419** |
| **Air Conditioner** | 49,698 | 23,538 | **26,160** |
| **Washing Machine** | 33,256 | 18,965 | **14,291** |
| **Television** | 37,569 | 21,958 | **15,611** |

---

## 📐 Mathematical Model

### Objective Function
Maximize total annual profit $Z$ (in BDT):

$$\text{Maximize } Z = 16419 X_1 + 26160 X_2 + 14291 X_3 + 15611 X_4$$

---

### Constraints

#### A. Annual Production Capacity Constraints
- $X_1 \le 2,300,000$ (Refrigerators & Freezers)
- $X_2 \le 180,000$ (Air Conditioners)
- $X_3 \le 80,000$ (Washing Machines)
- $X_4 \le 800,000$ (Televisions)

#### B. Total Budget Constraint
- $20850 X_1 + 23538 X_2 + 18965 X_3 + 21958 X_4 \le 54,400,000,000\text{ BDT}$

#### C. Raw Material Supply Constraints (Annual Limits)
- **Aluminum (kg):** $2.5 X_1 + 4.33 X_2 + 1.5 X_3 + 1.2 X_4 \le 10,000,000$
- **Steel (kg):** $34.67 X_1 + 30.5 X_2 + 35.3 X_3 + 0.5 X_4 \le 100,000,000$
- **Copper (kg):** $0.55 X_1 + 1.98 X_2 + 1.71 X_3 + 0.2 X_4 \le 35,000,000$
- **Plastic (kg):** $8.35 X_1 + 7.7 X_2 + 3.42 X_3 + 9.1 X_4 \le 25,000,000$
- **Glass (kg):** $1.4 X_1 + 1.8 X_2 + 0.79 X_3 + 1.9 X_4 \le 4,000,000$
- **Rubber (kg):** $0.91 X_1 + 0.63 X_2 + 0.41 X_3 + 0.2 X_4 \le 2,200,000$

#### D. Non-Negativity Constraints
- $X_1, X_2, X_3, X_4 \ge 0$

---

## 📈 Results & Key Findings

The Linear Programming problem was solved using the **Excel Solver (Simplex LP)** engine.

### Optimal Product Mix
- **Freezer & Refrigerator ($X_1^*$):** $2,300,000\text{ units}$ *(Max Capacity)*
- **Air Conditioner ($X_2^*$):** $180,000\text{ units}$ *(Max Capacity)*
- **Washing Machine ($X_3^*$):** $28,621\text{ units}$
- **Television ($X_4^*$):** $75,842\text{ units}$

### Maximum Achievable Profit
$$\mathbf{Z^* = 42,445,795,541\text{ BDT / year}}$$

### Insights
1. **Freezer/Refrigerators** and **Air Conditioners** produce the highest relative profit margins, making it optimal to run their production lines at $100\%$ capacity.
2. Production of **Washing Machines** and **Televisions** is limited due to raw material bottlenecks (particularly rubber and plastic availability limits).

---

## 👥 Authors & Academic Context

- **Course:** Operations Research (IPE-307)
- **Institution:** Bangladesh University of Engineering and Technology (BUET)
- **Department:** Industrial and Production Engineering (IPE)
- **Supervisor:** Dr. Kais Bin Zaman, Professor, Dept. of IPE, BUET

**Project Members:**
1. An-nur Taiweb Rahman (ID: 1908047)
2. Md. Sadman Sakib Mithun (ID: 1908028)

*Date of Submission: March 03, 2023*