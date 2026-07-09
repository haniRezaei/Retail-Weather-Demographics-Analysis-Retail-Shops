# Retail-Weather-Demographics-Analysis-Retail-Shops
SQL, Power BI project analyzing how weather and customer demographics drive daily retail sales across multiple shop locations
Problem Statement

Daily sales fluctuate, but leadership lacks clarity on why. Understanding how weather conditions and customer demographics impact performance gives the business a foundation for better planning, staffing, and promotions.

Goal: Turn three disconnected data sources (sales, weather, customer survey) into a single analytical view that answers concrete operational questions, and translate those answers into recommended actions.
This single view is what Power BI connects to, no joins or transformations happen inside the report itself, which keeps the model fast and the logic auditable in one place.




 Dashboard Walkthrough

The Power BI file (Miami_retail_shop.pbix) has two pages: a main dashboard and a supporting seasonality pivot table.

Business QuestionVisual in the DashboardHow strongly do temperature and rainfall affect daily sales?Dual-axis line chart — daily sales_usd vs. avg_temp_f, with an is_rain slicer to isolate wet vs. dry daysWhich shop performs best, and why?Clustered column chart — average sales_per_customer by shop_name, controlling for traffic differences between locationsWho are our customers — families vs. singles, male vs. female?Two donut charts — gender split (pct_male / pct_female) and household split (pct_family / pct_single)Are there predictable seasonal patterns in sales?Page 2 pivot table — sales_usd and sales_per_customer broken down by Year → Quarter → Month → DayWhat actions would you take based on these insights?Recommendations summary (see Section 5) — designed to translate to a slide for leadership

Also on the dashboard: KPI cards for total customers and total sales, plus slicers for date range, weekend/weekday, and rain/no-rain, so a stakeholder can filter the whole page interactively instead of asking for a re-cut.


Note for the next iteration: the demographic donut charts currently show an overall split, not a trend — a stacked area/bar chart by month would answer the "how does this change over time" part of the customer question more directly. Flagging this here so it's an intentional, visible next step rather than a gap discovered later.

* Key Insights

Weather matters, but differently for temperature vs. rain. Sales track fairly closely with temperature (hotter days pull in more customers), while rain doesn't kill sales outright, it changes behavior, showing up more as a dip in walk-ins than a full drop in revenue.
Shop performance isn't just about traffic. Once sales are normalized per customer, the ranking between shops shifts — a store with fewer visitors can still be the top performer per head, which changes how "best shop" should be defined for staffing decisions.
Customer mix varies by day type. Families and singles don't split evenly across weekdays vs. weekends, which has direct implications for promotions and staffing schedules.
Sales have a seasonal rhythm. Certain months consistently outperform others, useful for inventory and staffing planning well ahead of the peak.



