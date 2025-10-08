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
- Ride Volume over Time  
- Cancellation analysis (by driver & customer)  
- Booking Status Breakdown
- Payment mode and ride type breakdowns  
- Interactive filters for dynamic exploration  

💡 **SQL Analysis:**
- Queries written to identify:
  - All Incomplete Rides  
  - All Rides-UPI  
  - All Successful Bookings  
  - Average customers Ratings per Vehicle 
  - Cancelled Rides By Customers
  - Rides Cancelled by drivers-personal and car related issues
  - Top 5 Customers- Highest rides
  - Total Booking Value Of Rides 

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
