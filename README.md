# SuperStore-Sales
# SuperStore Sales Analysis

## Overview
This project analyses sales transactions for a fictitious retail company using the **SuperStore Sales dataset**. The dataset comprises three tables:
- **Orders Table**: Transactional data on orders, products, customers, shipping, and sales.
- **Returns Table**: Tracks returned orders.
- **People Table**: Maps regional managers.

**Dataset Link**: [SuperStore Sales Dataset](https://public.tableau.com/app/sample-data/sample_-_superstore.xls)

## Key Dataset Columns

### Facts:
- **Sales**, **Profit**, **Discount**, **Quantity**

### Date Dimension:
- **Order Date**, **Ship Date**

### Geographical Dimension:
- **Region → State → City → Postcode**

### Product Dimension:
- **Category → Sub-Category → Product ID/Product Name**

### Customer Dimension:
- **Segment → Customer ID, Customer Name**

### People Dimension:
- **Region, Person**

## Calculated Columns
- **Profit Margin**: `Sum(Profit) / Sum(Sales)`
- **Return %**: `Returns Count / Order Count`
- **Profit per Order**: `Sum(Profit) / Order Count`
- **Selling Price per Unit (SP)**: `Sum(Sales) / Sum(Quantity)`
- **Cost Price per Unit (CP)**: `(Sum(Sales) - Sum(Profit) - Sum(Discount)) / Sum(Quantity)`
- **Shipment Time**: `Difference between Ship date and Order date`

## Business Case
The analysis addresses key business questions:
- **Customers**:
  - Which customers are non-viable due to low profitability?
  - Which segments contribute most to sales and profits?
- **Products**:
  - Which products are profitable but underperforming in sales?
  - Which low-margin products should be discontinued?
- **Geography**:
  - Which states have high sales but low margins?
  - Which regions need targeted strategies?
- **Cross-Analysis**:
  - Which products are profitable for specific customer segments?
  - Which states have high demand for high-margin products?

## Approach
1. **Exploratory Analysis**: Sales and margin comparison across different dimensions.
2. **Cluster Analysis**: Custom segmentation of States, Customers, and Products based on Sales and Profit Margin.
3. **Cross-tabulation**: Deep insights from Product vs. State, State vs. Customer, and Product vs. Customer clusters.

### **Colour Coding for Profitability Insights:**
- **Red = Loss**, **Green = Profit**
- **Darker shades = Higher/Lower Margin**

## Key Findings
1. **Selling Price is the Key Driver of Profitability**: Losses mainly occur due to low selling prices, not cost variations.
2. **Hidden Gems & Volume Titans Drive Profits**: These segments generate high margins (31-42%) and should be prioritised.
3. **Premium Niche Needs Market-Specific Approach**: Some profitable segments struggle in risky zones and among unviable customers.
4. **Struggling Line & Dead Stock Cause Heavy Losses**: Discontinuing low-performing SKUs and clearing excess stock is essential.
5. **Revenue Black Hole & High-Value Segments Require Intervention**: High sales but low margins indicate pricing and credit control issues.
6. **Strong Markets (Golden Markets & Margin Masters) Should Be Prioritised**: Focus on inventory allocation and growth strategies.
7. **Red Zone States Are a Major Loss-Maker**: Pricing issues and weak demand require a shift towards premium customer retention.

## Strategy Recommendations
1. **Optimise Pricing Strategies**:
   - Establish minimum pricing thresholds.
   - Implement differentiated pricing based on market strength.

2. **Enhance Sales Negotiation & Value Proposition**:
   - Train sales teams to limit unnecessary price reductions.
   - Improve service offerings to justify premium pricing.

3. **Discontinue Loss-Making Products**:
   - Phase out struggling product lines.
   - Bundle slow-moving products with high-demand items.

4. **Focus on High-Margin Customer Segments**:
   - Prioritise profitable customer segments.
   - Limit sales exposure to unviable customers and risky zones.

5. **Reallocate Inventory Based on Market Strengths**:
   - Increase stock for high-performing markets.
   - Reduce inventory in Red Zone States where demand is weak.

## Conclusion
By focusing on high-margin clusters, refining pricing strategies, discontinuing underperforming products, and strengthening credit controls, the company can **drive sustainable profitability**. Aligning product strategies with market strengths while minimising exposure to loss-making segments will ensure **long-term financial stability and growth**.
