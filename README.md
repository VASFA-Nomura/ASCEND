# ASCEND
Interactive toolkit for analyzing model rocket flight data using Arduino Nano 33 BLE and BMP390. Built for students with no coding required. Launch via Binder and explore 3D flight paths, sensor filtering, and event tracking with Voilà.


# Rocket Data Analysis Notebook (Arduino Nano 33 BLE + BMP390)

This interactive notebook is designed to analyze data from a model rocket flight, logged using an Arduino Nano 33 BLE Sense Rev2 with a BMP390 sensor. It is intended for student-friendly analysis with Voilà deployment support.

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
- Validates CSV from Arduino and sets up time-indexed DataFrame.

### **2. Compute Altitude and Velocity**
- Button: `Compute Altitude & Velocity`
- Uses barometric formula and vertical velocity estimation.

### **3. Mark Events (Launch to Landing)**
- Button: `Set Event Markers`
- Interactive step to mark key flight events via plot.

### **4A. Map Marker**
- Button: `Run Step 4A`
- Place Launch, Apogee, and Landing coordinates on a satellite map.

### **4C. Save Environment Data**
- Button: `▶ Run Step 4C`
- Input temp/wind and compute magnetic field values.

### **6. View Sensor Noise Summary**
- Button: `▶ Run Step 6`
- Summarizes pre/post-flight noise and variation for sensor inputs.

### **7. Run Filter Selection**
- Button: `▶ Run Step 7`
- View and apply noise-based filtering for each sensor.

### **8. View World Frame Orientation**
- Button: `▶ Run Step 8`
- Estimate orientation using Madgwick filter + transform acceleration.

### **9. View Corrected World Orientation**
- Button: `▶ Run Step 9`
- Improves orientation stability using small-angle corrections.

### **10. Run Z-Axis Kalman Filter**
- Button: `▶ Run Step 10`
- Fuses altitude, velocity, and acceleration via Kalman filter.

### **11. Estimate Event Positions**
- Button: `▶ Run Step 11`
- Set 3D coordinates of flight events, generate smooth path.

### **12. View Position Estimations**
- Button: `▶️ Run Step 12`
- Compare X, Y, Z positions and hypsometric altitude over time.

### **13. Run X&Y Kalman Filter**
- Button: `▶️ Run Step 13`
- Kalman smoothing of XY positions + trajectory visualization.

### **14. Run Flight Simulation**
- Button: `▶️ Run Step 14`
- Animate the rocket trajectory over time with playback control.

---

## 🌐 Deploy with Voilà
Launch with:
```
voila Data_Analysis4.ipynb
```

Or use Binder:
- Add `requirements.txt` with dependencies.
- Use this README.md and ensure the notebook is in the root directory.
