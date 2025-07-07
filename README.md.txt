# 🚗 Dynamic Pricing for Urban Parking Lots – Model 1

## Overview
This project simulates dynamic pricing for parking lots using real-time occupancy data. The goal is to balance demand and availability using a baseline linear pricing model.

---

## Model 1 – Baseline Linear Formula

Price = Previous Price + α × (Occupancy / Capacity)


- α = 5  
- Price is capped between ₹5 and ₹20  
- Simple and interpretable logic

---

## Tech Stack
- Python
- Pandas
- Google Colab

---

## Output Example

Time Step 1: ₹13.2
Time Step 2: ₹15.4
Time Step 3: ₹17.8



---

## Folder Structure
- `model1_baseline.ipynb` → Notebook file  
- `dataset.csv` → Dataset used  
- `README.md` → Project summary

---



---

## Model 2 – Demand-Aware Pricing

`Price = Previous Price + α × (Occupancy / Capacity) + β × QueueLength`

- α = 5, β = 0.5  
- Price is capped between ₹5 and ₹25  
- This model increases price more when queue is longer  
- Better reflects real-time demand pressure



---

## Model 3 – Competition-Aware Pricing

`Price = Prev_Price + α × (Occupancy / Capacity) + β × QueueLength – γ × Avg_Nearby_Price`

- α = 5, β = 0.5, γ = 0.3  
- This model accounts for pricing competition from nearby lots  
- If nearby price is lower, this model suggests adjusting our price down  
- We used a dummy nearby price = ₹12 (as actual not provided)

 
