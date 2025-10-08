# 🚗 Ola Analytics Dashboard

An interactive **Power BI Dashboard** and **SQL Data Analysis** project built to explore, analyze, and visualize ride booking patterns for a fictional Ola ride-hailing dataset.

---

## 📁 Project Overview

This project provides end-to-end insights into **Ola’s booking data**, uncovering trends in customer behavior, cancellations, and revenue.  
It combines **SQL analysis** and **Power BI visualization** to build a complete data analytics pipeline — from raw data to business insights.

---

## ⚙️ Tools & Technologies

- 🟨 **Power BI** – Dashboard creation & data modeling  
- 🧩 **SQL** – Data cleaning, aggregation & insights extraction  
- 📊 **Excel (.xlsx)** – Source dataset with 20,000 booking records  
- 🧠 **DAX Measures** – Used to calculate KPIs like cancellation rate, average fare, and driver performance  

---

## 📈 Key Insights

✨ **Dashboard Features:**
- Total Bookings, Revenue & Average Fare KPIs  
- Cancellation analysis (by driver & customer)  
- Booking trends by date, time, and city  
- Payment mode and ride type breakdowns  
- Interactive filters for dynamic exploration  

💡 **SQL Analysis:**
- Queries written to identify:
  - Most frequently canceled routes  
  - Peak booking hours  
  - Top performing cities  
  - Customer vs. Driver cancellation ratios  
  - Average fare per ride type  

---

## 📊 Dataset

**File:** `Bookings-20000-Rows.xlsx`  
**Records:** 20,000 rows  
**Columns Include:**
- `Booking_ID`  
- `Customer_ID`  
- `Driver_ID`  
- `Booking_Date`  
- `Pickup_City` / `Drop_City`  
- `Booking_Status` (Completed, Canceled by Driver, Canceled by Customer)  
- `Fare_Amount`  
- `Payment_Method`  
- `Ride_Type` (Micro, Mini, Prime, etc.)

---

## 🧮 Sample DAX Measure

```DAX
Cancelled Bookings =
CALCULATE(
    COUNTROWS('Bookings'),
    'Bookings'[Booking_Status] IN {"Canceled by Driver", "Canceled by Customer"}
)
