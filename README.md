# HIT Smart Campus Prototype

##  Overview
This project demonstrates a **Smart Campus Management System** for the **Haldia Institute of Technology** (HIT).  
It integrates **Waste Management**, **Water Quality Monitoring**, and **Air Quality Monitoring** into a single web-based platform.

The solution is developed using **FastAPI**, **Leaflet Maps**, and **Chart.js** for real-time simulation and dashboard visualization.

---

## Features

### 1. Waste Management (Simulation)
- Interactive **map of HIT Campus**.
- **Smart bins** with fill-level monitoring (color-coded).
- **Smart vehicles** assigned dynamically to collect from the nearest full bin.
- Vehicles follow **shortest path routes** with animated movement.
- Real-time **sidebar dashboard** showing:
  - Bin fill levels
  - Vehicle statuses (Idle/Busy)
  - Assignments history
  - Comparison stats
- **Auto Simulation Mode**: bins fill automatically, vehicles get assigned dynamically.
- Reset controls.
- Static marker for **Water Tap** with coordinates displayed.

### 2. Environmental Monitoring (Dashboard)
- **Air Quality** panel with **6 gauges** (NH3, Smoke, Alcohol, Benzene, CO₂, NOx).
- **Water Quality** panel with **2 gauges** (TDS, EC).
- Gauges behave like **speedometers** (color-coded: Green / Orange / Red).
- **Waste Management dashboard** replicating simulation stats.

### 3. Complaint System (QR Code)
- Users scan a **QR code** and submit complaints (bin overflow, water issues).
- Complaints appear in the **Dashboard Alert System** panel.

---

## Tech Stack
- **Backend:** FastAPI (Python)
- **Frontend:** HTML, CSS, JavaScript
- **Mapping:** Leaflet.js, Routing Machine, MovingMarker
- **Charts:** Chart.js
- **IoT Integration:** Blynk API
- **Hosting (Local):** Uvicorn

---

## How to Run Locally

1. Clone the Project
   ```bash
   git clone https://github.com/hit2025/smart-waste-management.git
   cd hit-smart-campus
   ```

2. Install Dependencies
   ```bash
   pip install fastapi uvicorn requests
   ```

3. Run Waste Simulation
   ```bash
   python app.py
   ```
   → Open [http://127.0.0.1:8000](http://127.0.0.1:8000)

   - Tab 1: **Simulation Map**
   - Tab 2: **Dashboard**

4. Run Real-Time Blynk Dashboard
   ```bash
   python blynk_dashboard.py
   ```
   → Open [http://127.0.0.1:8001](http://127.0.0.1:8001)

---

##  Sensor Integration
- **Water Quality (Blynk Pins):**  
  - `v0` → TDS  
  - `v1` → EC  

- **Air Quality (Blynk Pins):**  
  - `v3` → NH3  
  - `v4` → Smoke  
  - `v5` → Alcohol  
  - `v6` → Benzene  
  - `v7` → CO₂  
  - `v8` → NOx  

- **Bin Depth (Future Extension):** `v2`, `v9-v12`

---

##  HIT Campus Mapping
- **Bins:** 5 bins placed at fixed lat/long inside campus.  
- **Vehicles:** 3 vehicles generated near campus center.  
- **Tap:** One water tap near campus center.

---

##  Complaint System
- QR code provided to scan.  
- Users enter **phone number + complaint message**.  
- Complaints displayed in real-time dashboard alerts.

---

##  Impact
- **Smart, Pollution-Free Waste Management**.
- Promotes **Clean Water Access & Monitoring**.
- Enhances **Air Quality Awareness**.
- Encourages **Community Participation**.

---

##  Team VIDYUT
- Project under **Haldia Institute of Technology**  
- Registration No.: **TH12180**

