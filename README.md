# Optimal Airport Location Analysis

This project uses hierarchical clustering to determine optimal airport locations within the United States based on population density. By analyzing geographic and demographic data, the project aims to suggest airport placements that maximize accessibility for densely populated areas.

## Project Overview

The primary goals of this project are to:
- **Analyze U.S. city population data** and use it to suggest optimal locations for airports.
- **Utilize hierarchical clustering (Agglomerative Clustering)** to group cities based on proximity and population density.
- **Validate suggested locations** against actual large U.S. airports.

## Methodology

1. **Data Preparation and Preprocessing**:
   - Loaded and cleaned a dataset of U.S. cities, removing outliers (e.g., cities significantly far from the mainland) that could skew results.
   - Scaled population values logarithmically to aid in visualization, creating a scatter plot of city locations with point sizes indicating population density.

<img width="854" alt="Screenshot 2024-11-13 at 12 02 12 AM" src="https://github.com/user-attachments/assets/a9c4026b-6d64-4571-a416-e83375861020">

2. **Hierarchical Clustering**:
   - Used Agglomerative Clustering to group U.S. cities into 67 clusters, reflecting natural population groupings.
   - Applied Ward's method to minimize variance within clusters, generating a hierarchy to illustrate spatial relations between clusters.
   - Visualized clusters in a scatter plot, with each city color-coded by its assigned cluster.
     
<img width="927" alt="Screenshot 2024-11-13 at 12 02 33 AM" src="https://github.com/user-attachments/assets/cf91cd6e-5cc0-4eee-9d2b-ec1a40389140">

3. **Centroid Calculation**:
   - Calculated centroids (average latitude and longitude) for each cluster to suggest potential airport locations.
   - Displayed centroids on a scatter plot with red "X" markers and generated a dictionary output with each centroid’s coordinates.
     
<img width="918" alt="Screenshot 2024-11-13 at 12 02 55 AM" src="https://github.com/user-attachments/assets/b91b8b88-88dd-4c2d-8ab1-f26dd7edab83">

4. **Validation**:
   - Compared the suggested airport locations to actual large airports in the U.S. by calculating distances using the Haversine formula.
   - Computed the average distance between suggested locations and the closest real-life large airport to assess the model’s accuracy.

<img width="627" alt="Screenshot 2024-11-13 at 12 03 20 AM" src="https://github.com/user-attachments/assets/f52e7b8a-eaa8-4abd-955d-895cd8fe9d29">

5. **Ethical Considerations**:
   - Outliers were removed responsibly to maintain model relevance to densely populated areas.
   - Acknowledged potential impacts if the model were to be used in real-world applications, as airport placement affects community access and local economies.

## Results

- The model’s suggested locations achieved an average distance of **236.28 kilometers** from the nearest large airports, aligning reasonably well with existing infrastructure.
- While population density is a primary factor, further criteria would be needed in real-world airport planning, including geographic, environmental, and legal considerations.

## Installation and Usage

### Prerequisites

- Python 3.x
- Required libraries: `pandas`, `numpy`, `scipy`, `matplotlib`, `sklearn`

### Running the Project

1. **Download the Notebook**:
   - Download `Optimal-Airport-Location-Analysis.ipynb` from this repository.

2. **Install Dependencies**:
   - Open a terminal and run:
   ```bash
   pip install pandas numpy scipy matplotlib sklearn
3. **Open and Execute the Notebook**:
   -  Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab to follow       the workflow, including data visualization, clustering, and validation.
## Visualizations

This project includes several key visualizations:

1. **Population Density Scatter Plot**:
   - Shows U.S. cities on a map with point sizes scaled by population density.

<img width="854" alt="Screenshot 2024-11-13 at 12 02 12 AM" src="https://github.com/user-attachments/assets/a9c4026b-6d64-4571-a416-e83375861020">

2. **Clustered Cities Scatter Plot**:
   - Displays cities grouped by clusters, with different colors representing each cluster.

<img width="927" alt="Screenshot 2024-11-13 at 12 02 33 AM" src="https://github.com/user-attachments/assets/cf91cd6e-5cc0-4eee-9d2b-ec1a40389140">

3. **Centroid Plot**:
   - Marks calculated centroids with red “X” markers, indicating optimal airport locations.

<img width="918" alt="Screenshot 2024-11-13 at 12 02 55 AM" src="https://github.com/user-attachments/assets/b91b8b88-88dd-4c2d-8ab1-f26dd7edab83">

4. **Validation Plot - Large Airports in the United States**:
   - Compares the suggested airport locations with actual large airport locations, including distance markers.
     
<img width="627" alt="Screenshot 2024-11-13 at 12 03 20 AM" src="https://github.com/user-attachments/assets/f52e7b8a-eaa8-4abd-955d-895cd8fe9d29">
