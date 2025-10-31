# Airport-Authority-Data-Analysis-Power-BI-Dashboard
**📘 Overview**
This Power BI dashboard provides a comprehensive analysis of flight operations data for the year 2017. The goal is to help the Airport Authority monitor key flight performance metrics, identify operational inefficiencies, and gain actionable insights into flight delays, carrier performance, and traffic distribution.
The dataset includes details such as flight dates, origin and destination airports, flight times, delays, distances, and operational carriers.

**🎯 Objectives**
To visualize flight traffic patterns and distribution across global airports.
To analyze on-time performance and delay trends across months.
To identify top-performing and underperforming routes or airports.
To explore relationships between delay durations, distances, and flight timings.

**📊 Dashboard Structure**
Page 1 – Overview Dashboard
Contains high-level KPIs and filters for exploration.
KPIs:
✈️ Total Flights – 6M+ flights analyzed.
⏱️ Average Arrival Delay – 4.33 minutes.
✅ On-Time Percentage – 82%.
🛫 Total Distance Covered – 63 million+ miles.
Filters:
Month
Operating Carrier (OP_CARRIER)
On-Time Status (On Time / Delayed)
Visuals:
World Map: Displays total flights by origin airport (highlighting traffic hotspots).
KPI Cards: Present summary metrics for quick insights.
Slicers: Allow filtering by time, airline, and delay status.
Page 2 – Performance Analysis Dashboard
Focuses on delay patterns and performance metrics.
Visuals:
📈 Avg Arrival Delay by Month
Shows seasonal delay trends.
Delays peak during June–August (likely due to summer congestion and weather).
🏙️ Count of On-Time Flights by Destination
Identifies busiest and most punctual airports.
ATL, ORD, and DEN have the highest flight counts.
⏰ Average Arrival Delay by Departure Hour
Reveals time-based performance trends.
Late-night and early-morning flights show less delay, while afternoon flights tend to be more delayed.
📉 Distance vs Arrival Delay (Scatter Plot)
Shows that longer-distance flights generally have more stable arrival times, while short and medium-distance routes experience more delay variation.

**💡 Key Insights**
Busiest Airports: ATL, ORD, and DEN dominate in flight volume and on-time performance.
Seasonal Trend: Delay rates spike mid-year (June–August), suggesting congestion or weather disruptions.
Time-of-Day Effect: Midday departures tend to have higher delays compared to morning or night.
Carrier Variation: Some airlines consistently perform better, indicating more efficient scheduling and operations.
Distance Correlation: Delay doesn’t always increase with distance — shorter flights are more prone to operational bottlenecks.

**🧩 Tools & Techniques**
Tool Used: Microsoft Power BI Desktop
Data Source: 2017 Flight Performance Dataset
Transformations: Data cleaning, calculated measures (Avg Arrival Delay, On-Time %, Total Flights)
DAX Formulas Used:
Total Flights = COUNTROWS('2017')
Avg Arrival Delay = AVERAGE('2017'[ARR_DELAY])
OnTime % = 
DIVIDE(
    CALCULATE(COUNTROWS('2017'), '2017'[On-Time Status] = "On Time"),
    COUNTROWS('2017')
)

**🏁 Conclusion**
This dashboard helps the Airport Authority to:
Quickly identify patterns in flight punctuality and delay causes,
Improve air traffic scheduling,
Optimize resource allocation at busy airports, and
Monitor carrier and route performance over time.
The insights can support data-driven decision-making in improving flight operations, reducing delays, and enhancing overall passenger satisfaction.
