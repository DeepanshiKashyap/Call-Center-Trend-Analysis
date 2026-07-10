# Call-Center-Trend-Analysis

## Problem Statement
Customer support call centers generate large volumes of interaction data daily, but without structured analysis, patterns in call volume, SLA compliance, and customer sentiment often go unnoticed. This project analyzes one month of call center data (October 2020) to uncover trends in call volume, service level performance, and customer sentiment — helping identify operational bottlenecks and areas for improvement.

## Dataset
- **Source:** Kaggle — Call Center Dataset
- **Size:** 32,941 records
- **Time Period:** October 1–31, 2020 (full month)
- **Columns:** Call ID, Customer Name, Sentiment, CSAT Score, Call Timestamp, Reason for Call, City, State, Channel, Response Time (SLA status), Call Duration (minutes), Call Center Location

## Tools Used
- Microsoft Excel (Pivot Tables, Pivot Charts, Slicers, Conditional Formatting)

## Approach
1. **Data Cleaning:** Converted timestamps to proper date format, added helper columns for Day of Week and Week Number, retained missing CSAT scores as-is (rather than imputing) to preserve data integrity.
2. **Pivot Table Analysis:** Built six pivot tables covering call volume trends, day-of-week patterns, SLA compliance by location, sentiment by call reason, channel effectiveness (CSAT), and average call duration by reason.
3. **Visualization:** Created line charts (daily trend), column charts (day-of-week pattern), stacked bar charts (SLA performance), and clustered bar charts (sentiment distribution).
4. **Dashboard:** Combined key visuals into a single interactive dashboard with slicers for Call Center, Channel, and Reason for Call.

## Key Insights
- Billing Question dominates call volume — accounting for 23,462 of 32,941 calls (71%), far outweighing Payments (4,749) and Service Outage (4,730) combined. This signals a strong opportunity for self-service FAQ/portal improvements to deflect routine billing queries.
- Sentiment skews negative overall — Negative + Very Negative sentiment together make up 51.9% of all calls (17,089 of 32,941), compared to just 21.5% Positive + Very Positive. This points to a broader customer experience issue rather than an isolated incident.
- SLA breach rate is consistent across all locations (~12.5–13%) — Baltimore (12.6%), Chicago (12.9%), Denver (12.4%), and Los Angeles (12.7%) all show nearly identical "Above SLA" rates. This is a notable finding: SLA performance issues are systemic across the network, not tied to any single underperforming call center.
- Call volume is unevenly distributed across centers — Los Angeles/CA (41.7%) and Baltimore/MD (33.4%) together handle about 75% of total calls, while Denver/CO handles only 8.4%. This imbalance may warrant a review of staffing allocation or load-balancing across centers.
- Sentiment distribution is remarkably uniform across all four call centers — each location shows nearly the same proportion of Negative (~33%), Neutral (~27%), and Positive (~12%) sentiment, indicating the sentiment issue is a company-wide pattern rather than a location-specific service quality gap.
- Traditional Call-Center channel still leads — at 32% of total volume, ahead of Chatbot (25%), Email (23%), and Web (20%), suggesting automated/self-service channels haven't yet become the primary deflection point despite their availability.
- Daily call volume is stable and consistent — daily counts hover steadily between ~1,050–1,150 calls with no major spikes across the month, suggesting predictable, evenly distributed demand rather than volatile peak days.


## Dashboard Preview
![Dashboard Overview](screenshots/dashboard_overview.png)

## Data Limitations
- CSAT score was missing for ~63% of records; all CSAT-based analysis is calculated only on the subset where feedback was provided.
- Dataset covers a single month, so trends reflect intra-month patterns (daily/weekly) rather than long-term seasonal trends.
- No agent-level identifier was available in the dataset, so performance comparisons are made at the call center location and channel level instead.

## How to Use
1. Open `Call_Center_Dashboard.xlsx`
2. Navigate to the "Dashboard" tab to view the interactive summary
3. Use slicers to filter by Call Center, Channel, or Reason for Call
4. Individual pivot table breakdowns are available on their respective sheets

## Author
Deepanshi Kashyap 
