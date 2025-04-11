# 🇨🇦 Canadian Population Trend Analysis (2003–2023)

This project analyzes population distribution by age and gender across Canadian provinces using Statistics Canada’s API. It automates data retrieval, stores it in MongoDB, and visualizes key trends through interactive maps.

## 📌 Project Overview

- Fetches data from StatCan API for dimensions like age, gender, and geography from 2003 to 2023.
- Cleans and transforms JSON responses into Pandas DataFrames.
- Stores structured records in a MongoDB Atlas collection.
- Performs province-wise aggregation to calculate max population across key age brackets.
- Uses Geopy and Folium to map population trends and generate an interactive HTML map.

## 🚀 How It Works

1. **API Integration:**  
   Connects to the Statistics Canada SDMX REST API and retrieves population data based on selected dimensions.

2. **MongoDB Storage:**  
   Uses `pymongo` to store structured data into a cloud MongoDB collection for querying and aggregation.

3. **Data Analysis:**  
   Aggregates and compares population counts across age ranges like 'All ages', '15 to 19', and '60 to 65' for each gender.

4. **Mapping with Folium:**  
   Uses `Geopy` to geocode provinces and `Folium` to create a map with custom popups showing population stats.

## 🛠️ Tech Stack

- Python  
- Pandas & JSON  
- MongoDB Atlas  
- Statistics Canada API (SDMX)  
- Folium (Geospatial Mapping)  
- Geopy (Geocoding API)  
- Jupyter Notebook

## 🗺️ Sample Output

An interactive map saved as `Population_maxALLages.html` shows:
- Max population counts (age 15–19) across provinces.
- Gender-wise comparison.
- Popup details with province codes.

## 🧠 Key Learnings

- Handling nested API JSON structures and transforming into DataFrames.
- Working with NoSQL (MongoDB) for data insertion and aggregation.
- Using retry logic and error handling for robust geolocation services.
- Building real-world map-based data visualizations with Folium.
