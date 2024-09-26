# Geographic Visualization of the Dominican Republic Provinces

This project aims to represent the provinces of the Dominican Republic on a geographic map, displaying information related to population. We use geospatial data in **GeoJSON** format along with a tabular dataset that includes province names, coordinates, and population data.

## Data Used

### 1. GeoJSON File
The **GeoJSON** file containing the geographic boundaries of the provinces was obtained from the National Geographic Institute of the Dominican Republic (IDERD), available on their [Geoportal](https://geoportal.iderd.gob.do/).

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

## Usage

1. Load the provided GeoJSON file or download it from the IDERD Geoportal.
2. Create a DataFrame with the columns province, latitude, longitude, and population.
4. Run the script that will load the data and generate the choropleth or interactive map.

## Conclusion
This project allows for the geographic visualization of the provinces of the Dominican Republic and their associated data in a visually appealing manner, offering both static and interactive options.

## Credits
- Geospatial Data: Geoportal IDERD
- Code and Analysis: David Acosta Diaz

