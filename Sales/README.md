# Sales Report (Power BI)
![Overview](Images/overview.gif)

## Introduction
This dashboard is built for **commercial leads and product managers** to monitor sales performance and act quickly.  
It consolidates **sales performance**, **customer segments & geography**, and **time trends** into one interactive report—so stakeholders can compare like-for-like, spot opportunities/risks, and move from context to action.

With this report, stakeholders can answer:
- Which **drugs** and **customers** drive or drag **sales performance**?
- How does the revenue mix vary by **country**, **buyer type**, **gender**, and **age group**?
- What are the **time trends** (MoM/seasonality/weekly patterns) that should guide promotions and inventory?

The dataset used in this analysis comes from a **drug sales dataset** (inspired by the YouTube tutorial [Power BI Sales Dashboard](https://www.youtube.com/watch?v=ovQ9czcvotk)).

---

## Dashboard File
- **Interactive report:**  [Open in Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiMDNmMTZhOWItNTAwOC00ODE4LTljNjItODAyM2Y3NjA2MWJjIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9)

> For the best experience, open the report in full-screen on Power BI Service.

---

## Tools & Skills Demonstrated
- **Data modeling (Star schema):** FactSales + Date (marked as date table), clean relationships, dedicated Measure Table.
- **Power Query (M) ETL:** Robust shaping, type discipline, reusable Calendar; clear, auditable steps.
- **DAX for decision KPIs:** Time-intelligence, cohort/segmentation logic, dynamic Top/Bottom with adjustable N; blank-safe, context-aware patterns.
- **Interactive UX:** Field Parameters (metric switch), Map↔Chart & Heatmap↔Chart toggles, global slicers; dynamic titles/captions.

---

## Dashboard Overview


This sales dashboard contains **3 pages**, designed to guide stakeholders from a quick performance snapshot to customer segmentation and finally time trends.

---
### Page 1 — Performance (Top/Bottom)
*(Best vs worst performers)*

![Performance](Images/1.gif)

**Topics covered**
- Executive KPIs: Units Sold, COGS, Revenue, Profit, Profit Margin — with current vs previous month comparison.
- Dynamic ranking: Top/Bottom **products** and **customers** by the active metric (Revenue / Profit / Transactions / Units) with contribution share.
- Context-aware summaries: dynamic titles/captions that state the active metric and N.

**This page helps answer**
- Who/what is driving or dragging **sales performance** this period?
- How does the ranking change when you switch the metric (Revenue ↔ Profit ↔ Transactions ↔ Units)?
- What portion of total performance is concentrated in the current **Top-N** vs **Bottom-N** cohort?

**Insight**
- Revenue is often **concentrated in a small Top-N** set → opportunity for protection (inventory/SLAs) and smart bundling for mid-tier items.  
- **Rank shifts across metrics** (e.g., high Units but low Profit) reveal margin/price mix issues worth investigating.  
- **Margin vs Revenue** can diverge due to discounting, product mix, or COGS—growth in sales doesn’t always translate to profitability.  
- **Bottom-N** items carry risk (slow movers/low margin) and are candidates for price tests, targeted promos, or phase-out.

---

### Page 2 — Customer (Segments & Geography)
*(Customer profile & where revenue comes from)*

![Customer](Images/2.gif)

**Topics covered**
- Customer overview: **Total Customers** and **Average Revenue per Customer (ARPC)**.
- Revenue by **Country** and **Buyer Type** (e.g., seller vs user) with comparative panels.
- Demographic splits: **Gender** and **Age Group**.
- Geographic callouts: highlight revenue share and pockets of growth.

**This page helps answer**
- Which **countries** and **buyer types** lead revenue and deserve focus?
- How do **gender/age** cohorts differ in behavior and basket size?
- Where are the **geo pockets** for expansion vs retention plays?

**Insight**
- Revenue is typically **skewed toward a few countries** → prioritize local playbooks (pricing, promos, inventory) in those markets.
- **Buyer Type** patterns often diverge (price sensitivity, basket composition) → run **segmented campaigns** and tailored offers.
- **Gender/Age** splits signal content and channel preferences → **personalize creative** and cadence.
- Emerging markets with **consistent ARPC** but lower penetration are prime targets for **growth sprints**.

---

### Page 3 — Time Trend (MoM & Seasonality)
*(Momentum, seasonality, and weekday patterns)*

![Time Trend](Images/3.gif)

**Topics covered**
- Monthly trajectory with **MoM deltas** to assess short-term momentum.
- **Yearly / Quarterly** revenue trend for structural shifts.
- **Weekday sales** profile and **top-selling drugs by day** (heatmap/chart view).
- KPI context for **Transactions** (transaction count) and **Total Revenue**.

**This page helps answer**
- What is the month-over-month direction of sales, and how stable is the momentum?
- Where do seasonal inflection points occur across quarters and years?
- Which weekdays concentrate demand, and which products drive those spikes?

**Insight**
- **MoM momentum ≠ long-term trend**: temporary dips/spikes need confirmation against the quarterly trajectory.  
- Clear **seasonality** suggests aligning campaigns, pricing, and inventory buffers with peak windows.  
- **Weekday concentration** enables precise timing for promos and staffing; top-by-day products reveal bundle and cross-sell candidates.  
- Monitoring **transactions vs revenue** uncovers mix effects (ticket size vs volume) that impact margin planning.

---

## Conclusion

This report establishes a **three-step decision path**:  
1) **Performance** pinpoints what to act on now (by metric, Top/Bottom, N).  
2) **Customer** shows where to focus (segments & geographies).  
3) **Time Trend** clarifies when patterns shift (MoM, seasonality, weekdays).

By combining **time intelligence**, **dynamic Top/Bottom ranking**, and **interactive field parameters**, the dashboard moves beyond static reporting into a **scenario tool**—helping teams align quickly, prioritize with confidence, and translate insight into action.