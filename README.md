# ✈ Airline Route Analysis & Profitability Model
**Capital One Data Challenge Submission**  
Repository: [Devipriya‑Dasari/airline-data-analysis-challenge](https://github.com/Devipriya-Dasari/airline-data-analysis-challenge)

---

## 🚀 Project Overview
This project analyzes **U.S. domestic flights** to identify **profitable routes for a new airline**. It combines **operational metrics** (delays, cancellations, occupancy) with **financial modeling** (ticket revenue, baggage fees, costs, and profit) to recommend **optimal routes and airports** for market entry.

---

## 🎯 Challenge Objective
- Identify **high-performing vs high-risk airports and routes**  
- Model **route-level profitability**  
- Recommend **top 5 routes for a new airline**  
- Provide **visual insights** for decision-making  

---

## 📊 Dataset Overview
- **Flights.csv:** Flight-level details (origin, destination, distance, occupancy, delays)  
- **Tickets.csv:** Ticket fares and passenger counts for round-trip flights  
- **Airport_Codes.csv:** Airport metadata (type, country, IATA codes)  

**Filters applied:**  
- Only **U.S. medium and large airports**  
- Only **non-cancelled flights**  
- Only **round-trip tickets**  

---

## 🛠 Methodology

### 1. Data Cleaning & Preprocessing
- Converted numeric columns (`DISTANCE`, `OCCUPANCY_RATE`, `DEP_DELAY`, `ARR_DELAY`, `ITIN_FARE`, `PASSENGERS`)  
- Removed cancelled and invalid flights  
- Focused on **U.S. medium/large airports**  
- Created **route identifiers** for round-trip aggregation  

### 2. Aggregation & Revenue Calculation
- Calculated **average ticket price per route**  
- Aggregated flight metrics: distance, occupancy, departure & arrival delays  
- Merged flight data with ticket revenue for **route-level financials**  

### 3. Cost & Profit Modeling
**Assumptions & Constants:**  
- Seats per flight: 200  
- Bag fee per passenger: $70 (round-trip)  
- Fuel & crew cost per mile: $8  
- Other costs per mile: $1.18  
- Airport fees: $10,000 per airport  
- Delay cost: $75 per minute beyond 15 min  

**Calculations:**  
- Total revenue = ticket revenue + baggage fees  
- Total cost = fuel/crew + airport fees + delay costs  
- Profit per flight = revenue − cost  
- Total profit = profit × number of round-trip flights  

### 4. Top Routes Identification
- **Top 10 busiest routes** by flight volume  
- **Top 10 most profitable routes**  
- **Recommended 5 routes** based on total profit and breakeven analysis  

---

## ✨ Key Insights
- High-traffic routes are not always the most profitable  
- Certain **medium-traffic airports** provide better profitability due to fewer delays  
- **Breakeven analysis** shows number of flights required to recover $90M aircraft cost  
- Early morning flights and specific hubs reduce delay costs, increasing profitability  

