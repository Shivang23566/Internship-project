# Internship-project
Landslide Susceptibility Mapping & Early Warning System 
A data-driven project using machine learning and geospatial analysis to identify landslide-prone areas in the Indian Himalayas and develop a framework for a rainfall-based early warning system.

# Project Goals
Develop a high-resolution Landslide Susceptibility Map for a chosen district (e.g., Shimla) by identifying the static geological and topographical factors that contribute to slope instability.

Design a prototype for a dynamic Early Warning Model that uses rainfall as a trigger to predict the short-term probability of a landslide in high-risk zones.

# Tech Stack & Tools
Language: Python

Core Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

Geospatial Libraries: GeoPandas, Rasterio, GDAL

GIS Software: QGIS for data visualization and pre-processing

Environment: Jupyter Notebooks

# Workflow & Methodology
The project follows a standard geospatial machine learning workflow:

Data Collection: Gathered diverse datasets including:

Digital Elevation Model (DEM) from ISRO's Bhuvan (CartoDEM)

Land Use/Land Cover (LULC) maps from ISRO

Geological and Soil Data from the Geological Survey of India (GSI)

Historical Landslide Inventory from GSI and local reports

Rainfall Data from the India Meteorological Department (IMD)

Feature Engineering: Derived key causative factors from the raw data using QGIS and Python:

Slope

Aspect (Slope direction)

Elevation

Curvature

Distance to Rivers

Distance to Fault Lines

# Model Training:

A balanced dataset was created using historical landslide points (positive class) and randomly sampled non-landslide points (negative class).

A Random Forest Classifier was trained to learn the relationship between the features and landslide occurrence.

#Susceptibility Map Generation:

The trained model was used to predict the landslide susceptibility probability for every single pixel (30x30m area) in the study region.

The final map was classified into five zones: Very Low, Low, Medium, High, and Very High risk.

 # Key Features
High-Resolution Risk Zonation: Provides a detailed (30m) susceptibility map, offering granular insights compared to traditional, broader maps.

Feature Importance Analysis: Identifies the most significant contributing factors to landslides in the region (e.g., is slope more important than land cover?).

Rainfall Threshold Calculation: Establishes a baseline for the amount of rainfall that could trigger events in high-risk zones, forming the basis for an early warning system.

 # Future Work
Integrate near-real-time rainfall data from IMD or satellite sources via an API.

Expand the study area to cover other vulnerable districts in Himachal Pradesh.

Experiment with deep learning models (e.g., Convolutional Neural Networks) for potentially higher accuracy.

Develop a simple web application using Streamlit or Flask to visualize the map and the real-time risk.

# License
This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgements
A sincere thank you to the following organizations for making their data publicly available:

Indian Space Research Organisation (ISRO)

Geological Survey of India (GSI)

India Meteorological Department (IMD)
