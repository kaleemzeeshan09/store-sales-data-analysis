# store-sales-data-analysis
Excel dashboard analyzing apparel store sales, orders, and customer demographics across channels and states.
# Store Sales Data Analysis Dashboard

## Business Problem
An apparel retailer sells across multiple online channels (Amazon, Flipkart, Myntra, Meesho, 
Ajio, Nalli, and others) across various Indian states. With sales spread across so many 
channels, categories, and customer segments, the business lacks a single clear view of where 
revenue is actually coming from, which orders are failing to convert into revenue (cancellations, 
returns, refunds), and which customer groups to focus marketing and inventory on. This project 
builds that single view.

## Objective
The dashboard is designed to help store operations and marketing teams answer:
- How are monthly sales and order volumes trending across the year?
- What proportion of orders are actually being delivered successfully versus 
  cancelled, refunded, or returned?
- Which states generate the most revenue?
- Which sales channel (Amazon, Flipkart, Myntra, Meesho, Ajio, Nalli, Others) is 
  driving the most orders?
- How do purchasing patterns differ between men and women, and across age groups 
  (Teenager, Adult, Senior)?
- Which product categories (Blouse, Bottom, Ethnic Dress, Kurta) and months are worth 
  filtering into for deeper analysis?
  
## Data Overview
The underlying dataset (`store-sales-data.xlsx`) contains order-level records including: 
order month, sales amount, order count, order status (Cancelled/Delivered/Refunded/Returned), 
customer gender, customer age group, state, product category, and sales channel. The dashboard 
sits on top of this data with four interactive slicers — Month, Category, Channel — allowing 
any visual to be filtered down to a specific slice of the business.

## Tools & Approach
- **Tools:** Excel (Pivot Tables, Pivot Charts, Slicers, combo charts for dual-axis comparisons)
- **Approach:** The raw order data was cleaned and structured into pivot tables, then visualized 
  using a mix of chart types chosen to fit each question — a combo chart (bars + line) for the 
  monthly sales-vs-order-count trend, a line chart for order status funnel, pie charts for 
  gender split, a horizontal bar chart for state ranking, a clustered column chart for age vs 
  gender, and a column chart for channel share. All visuals share the same slicers so the whole 
  dashboard updates together as filters are applied — for example, filtering to just the 
  "Kurta" category updates every chart to reflect only Kurta sales.

## Key Findings

### Monthly Sales & Order Trend
Sales (bars) and order count (line, secondary axis) were tracked from January through 
December. Sales peaked in the January–March window at close to 1.9M–2.0M, then declined 
through the middle and later months, dropping to roughly 1.4M–1.5M by around October–November 
before a slight recovery. This suggests a seasonal pattern where the business does 
disproportionately well in the early part of the year and softer through mid-to-late year — 
useful for planning inventory build-up and promotional timing in advance of the strong months.

### Order Status Funnel
Out of all orders tracked, 28,641 were successfully **Delivered**, while 1,045 were 
**Returned**, 844 were **Cancelled**, and 517 were **Refunded**. The delivered volume 
overwhelmingly dominates the funnel, which is a healthy sign, but the combined ~2,400 
orders that didn't result in a completed sale (cancelled + refunded + returned) still 
represent a segment worth investigating — particularly the Returned orders, which are 
more than double the Cancelled and Refunded volumes combined.

### Gender Split
Women account for 64% of sales, versus 36% for men — meaning close to two-thirds of 
revenue comes from female customers, a strong signal for how merchandising and marketing 
creative should be weighted.

### Top 5 States by Sales
Maharashtra leads with 2.99M in sales, followed by Karnataka (2.65M), Uttar Pradesh (2.10M), 
Telangana (1.71M), and Tamil Nadu (1.68M). Maharashtra and Karnataka together account for 
a substantial share of the top-5 total, suggesting these two states are the highest-priority 
markets for regional stocking and logistics planning.

### Age vs Gender Breakdown
Across every age group, women order at a higher rate than men:
- **Adults:** Women 34.59% vs. Men 15.47% — the largest single segment in the entire 
  dataset, and the clearest priority group.
- **Teenagers:** Women 21.13% vs. Men 9.20%.
- **Seniors:** Women 13.70% vs. Men 5.91% — the smallest segment overall, but still shows 
  the same gender pattern.

Adult women are, by a wide margin, the dominant customer segment across the business.

### Channel Performance
Amazon is the clear leader in order share at 35.5%, followed by Myntra (23.4%) and 
Flipkart (21.6%). The remaining channels — Nalli (4.8%), Meesho (4.5%), Others (4.1%), 
and Ajio (6.2%) — each contribute a much smaller share individually, but collectively 
still represent close to a fifth of total order volume, meaning they're not negligible 
even though no single one of them competes with the top three.

## Business Recommendations
1. **Double down on Adult women as the core segment** — merchandising, ad targeting, and 
   new product lines should be built primarily around this group's preferences, since they 
   drive the largest share of both gender and age-based demand.
2. **Prioritize Maharashtra and Karnataka for regional operations** — faster fulfillment, 
   localized promotions, or dedicated inventory buffers in these two states would protect 
   the highest-revenue markets.
3. **Invest further in Amazon, Myntra, and Flipkart** since they already drive the majority 
   of order volume, while monitoring the smaller channels (Ajio, Meesho, Nalli, Others) for 
   any channel showing early growth momentum worth doubling down on.
4. **Investigate the Returned-orders segment specifically** (1,045 orders) since it's larger 
   than Cancelled and Refunded combined — understanding *why* customers return items (sizing, 
   quality, mismatch with expectations) could meaningfully reduce this leakage.
5. **Plan inventory and campaigns around the January–March peak** identified in the monthly 
   trend, ensuring stock and marketing spend are front-loaded rather than spread evenly 
   across the year.

## Limitations
This analysis is based on historical order-level data and does not account for external 
factors such as seasonal promotions run by competitors, changes in channel commission 
structures, or shifts in customer acquisition cost — all of which would need to be layered 
in for a complete strategic view.

