
---

# 🚲 Daily Bike Trips in Washington D.C. – Data Mining Project

## 📌 Project Idea

This project analyzes **daily bike trip patterns** in Washington, D.C.’s bike-sharing system.
By combining **trip records**, **weather data**, **bike station locations**, and **urban features** (like bus stops, CBD areas, and parking zones), we uncover **spatial, temporal, and behavioral patterns** in bike usage.

The ultimate goal is to:

* Understand **when, where, and why** people ride bikes.
* Explore the **impact of weather and geography** on demand.
* Apply **data mining & predictive modeling** to forecast revenues and discover hidden usage patterns.

---

## 🛠️ Techniques & What I Learned

This project gave me hands-on exposure to a wide spectrum of **data science concepts** applied in practice:

### 🔹 Data Collection & Integration

* Downloaded & merged **heterogeneous datasets** (trips, weather, stations, bus stops, parking zones, CBD polygons).
* Learned to handle **spatial data** with `GeoPandas`, `shapely`, and `folium`.
* Ensured **coordinate system consistency (CRS)** for accurate geospatial analysis.

### 🔹 Data Cleaning & Preprocessing

* **Missing values** in trip station IDs filled via **spatial joins** (nearest station mapping).
* **Outlier detection**: removed trips outside D.C. boundaries and unrealistic ride durations.
* Solved **duplicate ride_id issues** and standardized datetime formats.

💡 *Lesson:* Real-world datasets are messy. I gained strong skills in **data validation, geospatial joins, and anomaly detection**.

### 🔹 Feature Engineering

Created new features to enrich analysis:

* **Trip duration & cost calculation** (depending on bike type, membership, CBD fees).
* **Station capacity categories** (small/medium/large) using quantiles & domain heuristics.
* **Proximity features**: distance to nearest metro/shuttle stops (using `BallTree` for efficiency).
* **Geohash encoding** for spatial segmentation.
* **Binary features** for CBD trips, “far from transit”, and closeness to city center.

💡 *Lesson:* Feature engineering is where **domain knowledge meets data science**. It makes raw data useful for deeper models.

### 🔹 Exploratory Data Analysis (EDA)

* Visualized temporal trends (daily, monthly, seasonal).
* Used **heatmaps & KDE plots** to explore trip densities.
* Discovered relationships between **weather variables** and trip demand.

💡 *Lesson:* Visualization helped translate millions of rows into **stories about mobility behavior**.

### 🔹 Advanced Data Mining Methods

* **Clustering (KMeans, DBSCAN, Agglomerative)** to detect hidden usage patterns across stations & users.
* **Time-series forecasting** with `Prophet` and `STL decomposition` to model daily revenue and seasonal demand.
* **Random Forest Regression** for predictive modeling and feature importance analysis.

💡 *Lesson:* Applying multiple models taught me **when to use clustering vs. prediction vs. forecasting**.

---

## 📊 Tools & Libraries

* **Python stack:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `plotly`
* **Spatial analysis:** `geopandas`, `shapely`, `folium`, `BallTree`, `geohash`
* **Modeling & forecasting:** `Prophet`, `STL`, `RandomForestRegressor`, clustering algorithms

---

## 🚀 Results

* Built a **clean integrated dataset** for millions of bike trips.
* Extracted meaningful **spatio-temporal insights** (who rides, when, and where).
* Identified the **impact of weather, station size, and location** on demand.
* Forecasted future revenues and discovered **clusters of stations** with similar usage patterns.

---

## 📖 Key Takeaways

This project was more than an analysis — it was a **data science journey**:

* Learned to **wrangle large, messy, geospatial datasets**.
* Discovered how **feature engineering shapes model performance**.
* Practiced **clustering, forecasting, and predictive modeling** in a real-world urban mobility context.
* Appreciated how data mining can **support smart city planning** and sustainable transportation.

---

✨ Whether you’re interested in **urban mobility**, **geospatial analytics**, or just love seeing how raw data turns into insights — this project shows the power of data mining in action.

---
