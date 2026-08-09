# San Francisco Bike Share Program Analysis

## Project Goal

Analyze usage patterns and operational performance of the SF Bike Share system to identify peak demand periods, underutilized assets, and user behavior trends.

## Business Questions Answered

1. **When do riders use the system most?** → Morning rush (7 AM–9 AM) accounts for 40% of daily trips; Tuesday–Thursday peak (345K–349K trips/day)
2. **Which stations are bottlenecks?** → Ferry Building/Embarcadero corridor handles 9.2K trips (top route)
3. **Which stations underperform?** → 20 stations have turnover < 0.5; expansion to underutilized areas needed
4. **Who uses the service?** → 75% male, 23% female; age 31–50 are primary users (619K trips)
5. **Regional viability?** → San Francisco dominates (1.45M trips); Oakland/Berkeley show lower adoption

## Dashboard Structure

### Page 1: Executive Overview
- Key metrics: 2M trips, 493 stations, 1,406 active days, 16.8 min average duration, 45 avg user age
- Comparison modes: Overall dynamics vs. Period comparison (MoM, QoQ, YoY)
- Executive summary for stakeholders

### Page 2: Usage by Day of Week
- Trip volume by weekday (peaked weekdays: 345K–349K; weekend drop to 132K–153K)
- Average duration by day (Saturday longest at 32 min; weekdays ~14–16 min)
- Time-of-day distribution (morning commute dominates)
- Heatmap: Trips by time-of-day across weekdays

### Page 3: Regional & Monthly Analysis
- Trips by region with interactive map
- Regional performance comparison (San Francisco 70%+, others <5%)
- Monthly trends (peak April/September at 150K trips)
- Stacked area charts showing regional mix over time

### Page 4: Station Geography
- Interactive map of 493 stations (bubble size = usage volume)
- Top 20 stations by trip volume (ranked)
- Geographic concentration in downtown SF (Ferry Building area)

### Page 5: Station Performance & Routes
- Top 20 routes by volume (Ferry Building ↔ Embarcadero: 9.2K trips)
- Underutilized stations map (turnover < 0.5)
- Top-20 lowest-performing stations identified for potential decommissioning

### Page 6: User Demographics
- Customer type distribution: 50% Subscribers, 40% Customers, 9% Unidentified
- Gender breakdown: 76% Male, 23% Female, 1% Other
- Age group analysis: 31–40 is largest segment (325K trips)
- Cross-tabulation: Trips by age group × time-of-day × day-of-week

## Key Insights

- **Peak Demand Clarity:** Weekday commute drives 75% of traffic; weekends are 40% lower
- **Commuter Profile:** 45-year-old male professionals; morning rush (6 AM–9 AM) = 40% of day
- **Geographic Concentration:** Downtown SF is 1.45M trips (72%); satellite regions <5% each
- **Station Efficiency Issue:** Top station (Ferry/4th) does 73K trips/year; bottom 20 combined do <50K
- **Route Optimization:** Top 20 routes = 120K trips (50% of total); network highly concentrated
- **Seasonal Pattern:** June–September peaks; Oct–May decline (summer tourism/commuting)

## Techniques Used

- **DAX Measures:**
  - Period comparisons: `MoM % = (Current Month - Previous Month) / Previous Month * 100`
  - YoY comparison with conditional formatting
  - QoQ relative performance
  - Rolling averages for trend smoothing

- **Data Modeling:**
  - Star schema with Date (year/month/quarter/day-of-week), Station (geography), User (type/age/gender), Route (origin–destination)
  - Pre-calculated time-of-day buckets (night, morning, day, evening)
  
- **Advanced Visualizations:**
  - Matrix table (cross-tabulation of age × day × time-of-day with 7×7 grid)
  - Geographic clustering (Bing Maps with dynamic bubble sizing)
  - Stacked area chart (monthly trends with regional stacking)
  - Heatmap formatting for time-of-day patterns
  - Waterfall logic in bar charts for trend clarity

- **Performance Optimization:**
  - Aggregated data to reduce visual lag
  - Pre-filtered date ranges to limit dataset size
  - Optimized DAX to reduce calculation overhead

## Files Included

- `bikeshare-dashboard.pdf` – Full 6-page dashboard export showing all analyses and visualizations
