# Visualización Geográfica de las Provincias de República Dominicana

Este proyecto tiene como objetivo representar las provincias de la República Dominicana en un mapa geográfico, mostrando información relacionada con la población. Utilizamos datos geoespaciales en formato **GeoJSON** junto con un conjunto de datos tabular que incluye nombres de provincias, coordenadas y población.

## Datos Utilizados

### 1. Archivo GeoJSON
El archivo **GeoJSON** que contiene los límites geográficos de las provincias fue obtenido del Instituto Geográfico Nacional de la República Dominicana (IDERD), disponible en su [Geoportal](https://geoportal.iderd.gob.do/).

### 2. DataFrame con Datos de las Provincias
El DataFrame contiene los siguientes campos:
- **Provincia**: Nombre de la provincia.
- **Latitud y Longitud**: Coordenadas geográficas de la provincia.
- **Población**: Población total de la provincia.

## Proceso

### 1. Carga de Datos
Se cargan los datos del archivo **GeoJSON** utilizando `geopandas` y los datos del DataFrame con `pandas`.

### 2. Unión de los Datos
Utilizamos el nombre de las provincias como clave para unir el **GeoDataFrame** del archivo **GeoJSON** con el DataFrame que contiene la población.

### 3. Creación del Mapa Coroplético
Generamos un mapa coroplético utilizando `geopandas` y `matplotlib`, donde cada provincia es coloreada según su población, empleando una escala de colores que va del naranja al rojo (`OrRd`).

### 4. Mapa Interactivo (Opcional)
También ofrecemos una opción para visualizar un mapa interactivo utilizando `folium`. Este mapa muestra los puntos donde están ubicadas las provincias, y se pueden agregar marcadores para visualizar la población en cada una.

## Cómo Ejecutar el Proyecto

### Requisitos
1. Python 3.x
2. Instalar las siguientes librerías:
   ```bash
   pip install pandas geopandas matplotlib folium shapely

## Uso

1. Cargar el archivo GeoJSON proporcionado o descargarlo del geoportal IDERD.
2. Crear un DataFrame con las columnas provinces, latitude, longitude, y population.
3. Ejecutar el script que cargará los datos y generará el mapa coroplético o interactivo.

##Conclusión

Este proyecto permite la visualización geográfica de las provincias de República Dominicana y sus datos asociados de manera visual y atractiva, con opciones tanto estáticas como interactivas.

### Créditos

- Datos geoespaciales: Geoportal IDERD
- Código y análisis: David Acosta Diaz
