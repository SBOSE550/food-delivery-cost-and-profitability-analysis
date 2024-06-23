# 🛵Food Delivery Profitability Analysis🛵
---------------------------------------
![dataset-cover](https://github.com/SBOSE550/food-delivery-cost-and-profitability-analysis/assets/98967373/a012e6e9-e735-42cf-b2a6-d3d294f75eb7)
## Overview
------------
This project involves an in-depth analysis of a food delivery company's profitability. The goal is to identify key factors influencing profit margins and to derive insights that can help improve operational efficiency and profitability.

## Dataset
-------------
The dataset used for this analysis includes the following columns:

- **Order ID:** A unique identifier for each order.
- **Customer ID:** A unique identifier for each customer.
- **Restaurant ID:** A unique identifier for each restaurant.
- **Order Date and Time:** The timestamp indicating when the order was placed.
- **Delivery Date and Time:** The timestamp indicating when the order was delivered.
- **Order Value**: Total value of the order.
- **Delivery Fee:** The fee charged for delivering the order.
- **Payment Method:** The method used by the customer to pay for the order.
- **Discounts and Offers:** The types of discounts or promotional offers applied to the order.
- **Discount Amount:** The monetary value of the discount applied to the order.
- **Commission Fee:** The revenue earned from commissions charged to restaurants.
- **Payment Processing Fee:** The fee charged for processing the customer's payment.
- **Refunds/Chargebacks:** The amount refunded to the customer or chargebacks incurred.
- **Profit:** Calculated as revenue minus the total cost.

## Analysis
-------------
The analysis focuses on the following aspects:

### Cost Analysis
- **Overview:** The cost analysis reveals that while the average cost is slightly lower than the revenue, the resulting profit is minimal.
- **Statistics:**
  - **Cost:** Maximum = 365.40, Minimum = 10.00
  - **Revenue:** Maximum = 200.00, Minimum = 50.00
  - **Profit:** Maximum = 180.00, Minimum = -298.90
- **Insight:** The business is experiencing significant losses due to high costs and low revenues.

### Revenue Analysis
- **Overview:** Most profit and loss occur when the commission percentage is between 0 and 50%.
- **Key Findings:**
  - **High Order Values:** Low commission percentages
  - **Low Order Values:** High commission percentages
- **Actionable Insight:** Increase the commission percentage for higher order values to boost revenue.

### Profitability Analysis
- **Overview:** Over time, the company has sustained major losses, with costs surpassing revenue, leading to extremely low profits.
- **Cost Contributors:**
  - **Discount Amount:** 56% of total cost
  - **Payment Processing Fee:** 22% of total cost
  - **Delivery Fee:** 21% of total cost
- **Key Insight:** Discount amounts are the primary contributor to high costs. Reducing discount amounts is crucial to decreasing overall costs.

    #### Discount Analysis
    - **Order Distribution:**
      - **No Discount:** 18.5% of total orders
      - **With Discounts:** 81.5% of total orders
        - **10% Discount:** 23.3% of total orders
        - **50-off Promo:** 20.1% of total orders
        - **15% for New Users:** 19.8% of total orders
    - **Profit Impact:**
      - **Losses:** Primarily due to 15% new user discounts and 10% discounts when applied to higher order value
      - **Profits:** Mainly from no discount and 50-off promo orders and when 15% new user discounts and 10% discounts applied to lower order values
    - **Key Insight:** Higher discount amounts result in greater losses, especially for high order values.

## Tools Used
- **Python:** For data analysis and visualization.
- **Pandas:** For data manipulation and cleaning.
- **NumPy:** For numerical operations.
- **Matplotlib and Seaborn:** For data visualization.
- **Jupyter Notebook:** For interactive analysis and documentation.

## Recommendations
-----------------------
Based on the insights from the analysis, the following recommendations aim to decrease costs, increase revenue, and consequently, significantly enhance profitability.

### 1. Cost Reduction:
- **High-Value Orders:** For orders where the order value exceeds 1000 and currently have a '10%' discount:
  - Replace 70% of these orders with a '50-off promo'.
  - Replace the remaining 30% with 'No discount'.
  - **Reason:** This approach leverages the fact that '50-off promo' and 'No discount' orders have shown better profitability.
- **Low-Value Orders:** For orders where the order value is less than 500:
  - Replace all '50-off promo' discounts with a '10%' discount.
  - **Reason:** Lowering discounts for smaller orders helps balance the overall discount impact, maintaining customer incentives while reducing costs.
- **New Users:** Adjust the discount for new users:
  - Provide a '15%' discount only up to a maximum of 75.
  - **Reason:** This cap on new user discounts prevents high discount amounts from eroding profit margins on higher order values.

### 2. Revenue Boost:
- **Commission Fees:** To increase revenue, adjust the commission fee structure:
  - Increase the commission fee by 10% of the order value for every 500 increase in order value.
  - **Reason:** By aligning commission fees with order values, we can better capture revenue from higher-value orders, where the current commission is disproportionately low.
