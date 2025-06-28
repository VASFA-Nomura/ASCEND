![ASCEND](ascend-logo.png)

Interactive toolkit for analyzing model rocket flight data using Arduino Nano 33 BLE and BMP390. Built for students with no coding required. Launch via Binder and explore 3D flight paths, sensor filtering, and event tracking with Voilà.

# ASCEND Rocket Flight Data Analysis Notebook

This student-friendly interactive Jupyter notebook is designed for analyzing model rocket flight data captured using an Arduino Nano 33 BLE Sense Rev2 with a BMP390 sensor. It supports interactive visualizations, physics-based computations, and Voilà-compatible controls for educational deployment.

---

## 📦 Dependencies

Install these in your environment or use Binder/Voilà:
- numpy
- pandas
- matplotlib
- plotly
- ipywidgets
- ipyleaflet
- ahrs
- scipy
- filterpy
- scikit-learn

---

## 🚀 Workflow Overview

### **1. Load & Clean Data**
- Button: `Load Rocket Data`
- Validates and parses the Arduino CSV log into a DataFrame with time indexing.

### **2. Compute Altitude and Velocity**
- Button: `Compute Altitude & Velocity`
- Uses barometric pressure and finite differences to compute altitude and vertical velocity.

### **3. Mark Events (Launch to Landing)**
- Button: `Set Event Markers`
- Interactive plot to label key flight events (launch, burnout, apogee, etc).

### **4A. Map Marker**
- Button: `▶ Map Marker`
- Drag-and-drop launch/apogee/landing locations on a satellite map.

### **4C. Save Environment Data**
- Button: `Save Environment Data`
- Inputs local environmental conditions to estimate magnetic field and wind.

### **6. View Sensor Noise Summary**
- Button: `View Sensor Noise Summary`
- Compares sensor stability pre- and post-flight using CV (coefficient of variation).

### **7. Run Filter Selection**
- Button: `Run Filter Selection`
- Dynamically filter and smooth selected sensor data based on noise and events.

### **8. View World Frame Orientation**
- Button: `View World Frame Orientation`
- Uses Madgwick filter to compute orientation; converts acceleration to world frame.

### **9. View Corrected World Orientation**
- Button: `View Corrected World Orientation`
- Applies small-angle corrections and flattens drift in orientation estimates.

### **10. Run Z-Axis Kalman Filter**
- Button: `Run Z-Axis Kalman Filter`
- Applies Kalman filter to fuse vertical acceleration and barometric altitude.

### **11. Estimate Event Positions**
- Button: `Estimate Event Positions`
- Adjust 3D positions of key flight events and interpolate trajectory.

### **12. View Position Estimations**
- Button: `View Position Estimations`
- Plots X, Y, Z positions and compares with altitude measurements over time.

### **13. Run X&Y Kalman Filter**
- Button: `Run X&Y Kalman Filter`
- Kalman filter for horizontal motion; shows position, velocity, and full trajectory.

### **14. Run Flight Simulation**
- Button: `Run Flight Simulation`
- Animates 3D flight path with timeline slider and event markers.

---

## 🌐 Deploy with Voilà

To launch locally:
```bash
voila ASCEND_Data_Analysis.ipynb
