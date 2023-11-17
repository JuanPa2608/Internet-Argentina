#  <p align="center"> Conexiones a Internet en Argentina </p>
Proyecto desarrollado como 2do proyecto individual del curso Data Science de Henry. Se realizó un análisis del comportamiento del sector internet en Argentina. Se trabajó sobre los datos libres de https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/ 

Objetivos:
- Calidad de Servicio
- Identificar oportunidades de crecimiento
- Soluciones personalizadas

<p align="center"> <img width="600" height="350" src = "https://tn.com.ar/resizer/eNimDERtuXj0kwzOz9ZA1HYKKas=/767x0/smart/filters:format(webp)/cloudfront-us-east-1.images.arcpublishing.com/artear/D3TWUMYFS5A3RJEEEQVTHCIFFU.png"> </p>

#  <em> Extracción, Transformación y Carga (ETL) </em>

Se trabajo el siguiente archivo en Jupyter: https://github.com/JuanPa2608/Internet-Argentina/blob/main/ETL/ETL.ipynb

1- Se importó toda la información disponibles en la API, teniendo algunas respuestas al request de 500 indicando errores desconocidos.

2- La data importada cuenta con una columna de tags, se filtró los guids que estén relacionados a internet.

3- Incursionando en la página, se agregó manualmente otros guids relacionados o que puedan ser útiles para el análisis.

4- Con el fin de realizar un análisis personalizado, se importa también datos de latitud y longitud por localidad y provincia.

5- Finalmente toda la data extraída se pone a disposición en la carpeta https://github.com/JuanPa2608/Internet-Argentina/tree/main/datasets/Fuente 

#  <em> Análisis Exploratorio de Datos (EDA) </em>
