# Uber-Analysis-Dashboard 🚖

### Dashboard Link : [Click here to view the dashboard](https://app.powerbi.com/links/ZW5mey78dL?ctid=d4963ce2-af94-4122-95a9-644e8b01624d&pbi_source=linkShare)

---

## 📌 Problem Statement  

This dashboard helps Uber and ride-hailing companies better understand their **operations, demand patterns, and customer behavior**.  

It provides insights into:  
- Most **frequent pickup and drop-off points**  
- **Peak demand hours and weekdays vs weekends**  
- **Ride volumes in real time**  
- Total distance traveled and average trip duration  

By leveraging these insights, Uber can optimize **driver allocation, reduce waiting time, and improve operational efficiency**.  
The real-time functionality allows managers to **monitor live demand spikes** and act quickly.  

---

## ⚙️ Steps Followed  

- **Step 1** : Load Uber ride dataset (CSV/Excel) into Power BI Desktop.  
- **Step 2** : Open Power Query Editor & in *Data Preview*, check `Column distribution`, `Column quality`, and `Column profile`.  
- **Step 3** : Enable *column profiling for entire dataset* instead of default 1000 rows.  
- **Step 4** : Handle missing values in trip timestamps/coordinates.  
- **Step 5** : Transform columns (Date, Time, Day of week, Time Slots).  
- **Step 6** : Apply custom theme for visuals.  
- **Step 7** : Create **Map visuals** to show hotspots for pickups & drop-offs.  
- **Step 8** : Add **slicers** for Date, Time, Pickup Location, Drop Location.  
- **Step 9** : Create **Card visuals** for Total Trips, Avg Trip Duration, Total Distance.  
- **Step 10** : Add **bar chart** for trip counts segmented by hours of day.  
- **Step 11** : Add **line chart** for ride trends (daily/weekly).  
- **Step 12** : Add **heatmap visuals** to highlight top 10 pickup & drop zones.  
- **Step 13** : Insert company branding — text box (Uber Analysis) & logo image.  
- **Step 14** : Create calculated column to categorize trips into Time Slots (Morning, Afternoon, Evening, Night).  
- **Step 15** : Create DAX measures:  

```DAX
Total Trips = COUNT(UberData[Trip_ID])  
Total Distance Travelled = SUM(UberData[Distance])  
Avg Trip Duration = AVERAGE(UberData[Trip_Duration])  
```
- **Step 16** : Add KPI Card to highlight **real-time active trips**.  
- **Step 17** : Configure **Power BI Streaming Dataset / Push API** to enable live refresh.  
- **Step 18** : Publish the report to **Power BI Service**.  

---


## 💡 Insights  

The dashboard provides the following insights:  

### [1] Total Trips & Distance  
- **Total Trips** = ~500,000  
- **Total Distance Travelled** = ~3.8M miles  
- **Average Trip Duration** = ~12 minutes  

### [2] Frequent Locations  
- **Top 5 Pickup Points**: City Center, Airport, Business Districts  
- **Top 5 Drop-off Points**: Suburbs, Shopping Hubs, Universities  

### [3] Demand by Time of Day  
- **Morning (6–9 AM):** High airport/business demand  
- **Evening (5–9 PM):** Peak office commute and leisure trips  
- **Late Night (11 PM–2 AM):** Spikes on weekends (nightlife/entertainment)  

### [4] Day-wise Trends  
- **Weekdays:** Higher ride volume, shorter duration (work commute)  
- **Weekends:** Fewer rides, but longer average trip distances  

### [5] Real-Time Monitoring  
- Streaming visuals show **active trip counts updating live**  
- Allows managers to **deploy additional drivers during demand spikes**  

---

## ✅ Final Inference  

The **Uber Analysis Dashboard** highlights:  
- **Hotspots of demand**  
- **Peak ride hours**  
- **Real-time trip counts**  

These insights help Uber optimize **driver deployment, reduce waiting time, and improve customer experience**.  

---

## 🚀 How to Use  

1. Clone this repo.  
2. Add your own Uber dataset (`UberData.csv`).  
3. Open `.pbix` file in Power BI Desktop to explore.  
