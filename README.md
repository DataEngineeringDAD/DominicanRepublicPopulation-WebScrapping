# Geographic Visualization of the Dominican Republic Provinces

This project aims to represent the provinces of the Dominican Republic on a geographic map, displaying information related to population. We use geospatial data in **GeoJSON** format along with a tabular dataset that includes province names, coordinates, and population data.

## Data Used

### 1. GeoJSON File
The **GeoJSON** file containing the geographic boundaries of the provinces was obtained from [Cartography Vectors](https://cartographyvectors.com/map/1436-dominican-republic-with-regions).

### 2. DataFrame with Province Data
The DataFrame contains the following fields:
- **Province**: Name of the province.
- **Latitude and Longitude**: Geographical coordinates of the province.
- **Population**: Total population of the province.

## Process

### 1. Data Loading
The **GeoJSON** file is loaded using `geopandas`, and the DataFrame is loaded using `pandas`.

### 2. Data Merging
We use the province name as the key to merge the **GeoDataFrame** from the **GeoJSON** file with the DataFrame containing population data.

### 3. Creation of a Choropleth Map
We generate a choropleth map using `geopandas` and `matplotlib`, where each province is colored according to its population, utilizing a color scale that ranges from orange to red (`OrRd`).

### 4. Interactive Map (Optional)
We also provide an option to display an interactive map using `folium`. This map shows the points where the provinces are located, and markers can be added to display the population of each province.

## How to Run the Project

### Requirements
1. Python 3.x
2. Install the following libraries:
   ```bash
   pip install pandas geopandas matplotlib folium shapely

### Usage

1. **Load the GeoJSON file**: Use the provided GeoJSON file or download it from [Cartography Vectors](https://cartographyvectors.com/map/1436-dominican-republic-with-regions).
2. **Create a DataFrame**: The DataFrame should include the columns `province`, `latitude`, `longitude`, and `population`.
3. **Run the Script**: Execute the script, which will handle data loading and visualization to generate a choropleth or an interactive map.

### Conclusion

This project provides a clear and visually appealing representation of the Dominican Republic's provinces and their population data. The visualization can be adapted for both static and interactive displays, offering flexibility depending on the required output.

It serves as a useful tool for understanding the demographic distribution of the Dominican Republic and can be extended to include additional socio-economic indicators or datasets for more comprehensive insights.
