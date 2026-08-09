# Sports Shoes Market Analysis

## Project Goal

Analyze global sports footwear market trends (2018–2026) to identify growth opportunities, product performance, and geographic market potential.

## Business Questions Answered

1. **Which brands are market leaders by revenue?** → ASICS leads at 1.56M, followed by Nike and New Balance
2. **How effective are pricing strategies?** → Reebok shows the smallest gap between base and final prices (less discount-dependent)
3. **Which product categories drive revenue?** → Lifestyle category dominates across all brands
4. **What are the geographic opportunities?** → UK is the strongest market; Pakistan shows untapped potential
5. **How do payment methods affect sales?** → Bank Transfer is the preferred method (94%); Cash is rarely used

## Dashboard Structure

### Page 1: Executive Overview
- Key metrics: Total Revenue (9.08M), YoY% (12.3%), Units (75K), Average Bill ($302.71)
- Revenue by brand (bar chart showing equal distribution among top 6)
- Revenue by category and country
- Payment method breakdown

### Page 2: Product Analysis
- Price vs. Margin analysis across brands
- Top 10 models by revenue
- Sales volume by category
- Customer purchase patterns by income level and gender
- Rating distribution by price point

### Page 3: Sales Channel & Payment
- Sales channel breakdown
- Payment method frequency
- Customer acquisition by method

### Page 4: Trends & Geography
- Year-over-year revenue dynamics (2018–2026)
- Annual units sold trend
- Geographic revenue distribution
- Interactive map visualization (Bing Maps)

## Key Insights

- **Revenue Stability:** Market fluctuates between 0.97M–1.03M annually, with 12.3% recent growth
- **Discount Impact:** High discounts on some brands (18–19% reduction) indicate potential margin optimization
- **Product Mix:** Lifestyle shoes dominate but other categories show growth potential
- **Market Opportunity:** Underperforming regions (Pakistan, UAE) present expansion possibilities

## Techniques Used

- **DAX Calculations:**
  - YoY% change: `(Current Year - Previous Year) / Previous Year * 100`
  - Average transaction value: `Total Revenue / Units Count`
  - Margin: `(Average Base Price - Average Final Price) / Average Base Price * 100`

- **Data Modeling:** Star schema with Brand, Category, Country, and Date dimensions

- **Visualizations:**
  - Clustered bar charts for brand/category comparison
  - Combo charts (bars + line) for trend analysis
  - Pie/donut charts for distribution
  - Scatter plots for price-rating correlation
  - Interactive slicers for multi-dimensional filtering
