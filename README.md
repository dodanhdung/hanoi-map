# A* Algorithm Application on Real-World Maps

⭐ **A\* Algorithm Application on Real-World Maps Using OSMnx and NetworkX**
📌 *Course Project - Introduction to Artificial Intelligence (School of ICT, HUST)*

---

## 📌 Overview

This project implements the **A\* Search Algorithm** on real-world maps using data from **OpenStreetMap (OSM)**. The street network graph is built using the **OSMnx** and **NetworkX** libraries. The A\* algorithm is applied to find the shortest path between two points on a real-world transportation network (e.g., Hanoi, Vietnam).

---

## 📂 Features

✅ **Build Graph from OSM Data**:
&nbsp;&nbsp;&nbsp;- Extract real-world street networks.

✅ **A\* Algorithm Implementation**:
&nbsp;&nbsp;&nbsp;- Custom implementation of A\* without using built-in shortest path functions.

✅ **Visualization**:
&nbsp;&nbsp;&nbsp;- Display the graph and the calculated shortest path.

✅ **Interactive Web Interface**:
&nbsp;&nbsp;&nbsp;- Allows users to select start points, end points, and algorithms on an interactive map.
&nbsp;&nbsp;&nbsp;- (Via `Deploy.py` file using Flask and Leaflet).

✅ **Algorithm Comparison**:
&nbsp;&nbsp;&nbsp;- Provides the ability to compare A\* with other pathfinding algorithms like UCS (Dijkstra), Greedy BFS, and DFS.

---

## 📊 Road Data Attributes & Description

| Attribute | Description |
| :--- | :--- |
| **osmid** | ID of the road segment in OpenStreetMap |
| **highway**| Type of road (residential, primary, etc.) |
| **oneway** | Indicates if the road is one-way |
| **reversed**| Direction of the road when loaded from OSM (True if reversed from original drawing direction) |
| **length** | Length of the road segment (meters) |
| **geometry**| GPS data of the road segment (as a LINESTRING) |
| **lanes** | Number of lanes |
| **name** | Name of the road (if available) |

---

## 📌 Technology Stack Used

- **Python** 🐍
- **OSMnx** 🌍 (Extracts real-world street networks from OSM)
- **NetworkX** 🔗 (Graph representation and operations)
- **Matplotlib** 📊 (Graph visualization in Jupyter Notebook - `A_star.ipynb`)
- **Flask** 🌐 (Builds the web application backend - `Deploy.py`)
- **Leaflet.js** 🗺️ (Map display and interaction on the frontend - `index.html`)
- **NumPy** (Numerical computations, often used by OSMnx/NetworkX)
- **GeoPandas, Shapely** (Handling geospatial data, used by OSMnx)

---

## 🚀 How to Run the Web Application

1. **Install necessary libraries:**
   ```bash
   pip install osmnx networkx matplotlib numpy flask geopandas shapely
   ```
2. **Prepare the map data file:**
    * Ensure you have the `hanoi_inner_city_polygon_combined.graphml` file in the same directory as `Deploy.py` (or the corresponding `.graphml` file for your desired area).
    * This file can be generated from the `A_star.ipynb` notebook by using OSMnx to download and save data from OpenStreetMap for the desired region.
3. **Run the Flask application:**
    Open a terminal or command prompt, navigate to the project directory, and run the command:
    ```bash
    python Deploy.py
    ```
    The application will run on port 8000 by default.
4. **Access the application:** 
    Open a web browser and go to http://127.0.0.1:8000.
5. **Use the Interface:**
    * Click on the map to select the start and end points.
    * Or use the address search bar to select points.
    * Select the desired algorithm from the dropdown list.
    * Press the "Reset Points" button to reselect points.
    * The path and information (length, nodes visited, execution time) will be displayed.
---