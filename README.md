#  <p align="center"> Conexiones a Internet en Argentina </p>
Proyecto desarrollado como 2do proyecto individual del curso Data Science de Henry. Se realizó un análisis del comportamiento del sector internet en Argentina. Se trabajó sobre los datos libres de https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/ 

Objetivos:
- Calidad de Servicio
- Identificar oportunidades de crecimiento
- Soluciones personalizadas

<p align="center"> <img width="600" height="350" src = "https://tn.com.ar/resizer/eNimDERtuXj0kwzOz9ZA1HYKKas=/767x0/smart/filters:format(webp)/cloudfront-us-east-1.images.arcpublishing.com/artear/D3TWUMYFS5A3RJEEEQVTHCIFFU.png"> </p>

#  <em> Extracción, Transformación y Carga (ETL) </em>

Se trabajo el siguiente archivo en Jupyter: https://github.com/JuanPa2608/Internet-Argentina/blob/main/ETL/ETL.ipynb

1- Se importó toda la información disponibles en la API.

2- La data importada cuenta con una columna de tags, se filtró los guids que estén relacionados a internet.

3- Incursionando en la página, se agregó manualmente otros guids relacionados o que puedan ser útiles para el análisis.

4- Con el fin de realizar un análisis personalizado, se importa también datos de latitud y longitud por localidad y provincia.

5- Finalmente toda la data extraída se pone a disposición en la carpeta https://github.com/JuanPa2608/Internet-Argentina/tree/main/datasets/Fuente 

#  <em> Análisis Exploratorio de Datos (EDA) </em>
## GUID: ACCES-A-INTER-FIJO-16249
Número de accesos al servicio de Internet fijo por velocidad de bajada en cada localidad declarada.

1- Se normaliza el tipo de variables, duplicados y nulos.

2- Se totaliza todas las conexiones por Localidad.

3- Se une a la tabla de Localidad con latitud y longitud para dashboard. Archivo: https: https://github.com/JuanPa2608/Internet-Argentina/blob/main/datasets/Fuente/Localidades.parquet

4- Se grafica un pairplot con las variables numéricas, mostrándose:

- De acuerdo a la data, se presentan mayor cantidad de conexiones en la zona norte (mayor latitud).

- De acuerdo a la data, se presentan mayor cantidad de conexiones en la zona este (mayor longitud).

- La concentración de datos se presentan en los lugares de mayor latitud y longitud, es decir al noreste de Argentina. Es decir, se presentan mas conexiones en esa zona que corresponde a la capital Buenos Aires.

5- Se grafica un scatterplot con las conexiones por localidad, mostrándose:

- Las localidades Avellanda, Arrecifes y Adrogué al contar con mas de 2500 conexiones encabezan la cantidad de conexiones.

- Los que cuentan con menor cantidad de conexiones son 12 de Octubre, Lucas Monteverde y Vásquez juntos con la sección Otros.

6- Se guarda el nuevo dataframe generado en el archivo parquet: https://github.com/JuanPa2608/Internet-Argentina/blob/main/datasets/dataset_vis/vis_ACCES-A-INTER-FIJO-16249.csv

## GUID: INGRE-POR-LA-OPERA-DEL
Número total de accesos al servicio de Internet fijo por banda ancha y banda angosta (trimestral). De acuerdo a https://www.adslzone.net/esenciales/preguntas/que-es-banda-ancha/ , uno de los tipos de banda estrecha o angosta es dial up. Por lo cual la columna 'Total' debería ser la suma de 'Banda ancha fija' y 'Dial up'

1- Se normaliza el tipo de variables, duplicados y nulos.

2- Se totaliza los tipos de conexiones por Provincia.

3- Se une a la tabla de Provincia con latitud y longitud para dashboard. Archivo: https://github.com/JuanPa2608/Internet-Argentina/blob/main/datasets/Fuente/Provincias.parquet

4- Se grafica un pairplot con las variables numéricas, mostrándose:

- De acuerdo a la data, se presentan mayor cantidad de conexiones en la zona norte (mayor latitud).

- De acuerdo a la data, se presentan mayor cantidad de conexiones en la zona este (mayor longitud).

- La concentración de datos se presentan en los lugares de mayor latitud y longitud, es decir al noreste de Argentina. Es decir, se presentan mas conexiones en esa zona que corresponde a la capital Buenos Aires.

5- Se grafica un scatterplot con las conexiones por localidad, mostrándose:

- Las localidades Avellanda, Arrecifes y Adrogué al contar con mas de 2500 conexiones encabezan la cantidad de conexiones.

- Los que cuentan con menor cantidad de conexiones son 12 de Octubre, Lucas Monteverde y Vásquez juntos con la sección Otros.

6- Se guarda el nuevo dataframe generado en el archivo parquet: https://github.com/JuanPa2608/Internet-Argentina/blob/main/datasets/dataset_vis/vis_ACCES-A-INTER-FIJO-16249.csv
