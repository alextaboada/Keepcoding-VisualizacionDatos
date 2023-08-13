# Práctica de Visualización de datos

## Objetivo
Actuando como propietario de de Airbnb, y sabiendo que los ingresos de la empresa corresponden a un % de las reservas en la plataforma, me interesa analizar los ingresos y reservas del próximo año para calcular los beneficios, así como saber quienes son los propietarios que más ingresan con el fin de plantear posibles campañas de publicidad.

## Origen de datos
Los datos han sido sacados de la web [Inside Airbnb](http://insideairbnb.com/get-the-data/), consiguiendo los siguientes archivos solamente de la ciudad de Madrid:

- Listing.csv Archivo que contiene los diferentes inmuebles de la ciudad, con los datos del propietario y datos reseñables de cada inmueble. 
- Calendar.csv Archivo que contiene los 365 días siguientes para cada uno de los inmuebles, especificando si ese día está o no reservado y el precio de cada inmueble para ese día.
- Neighborhood.geojson Archivo que contiene información geográfica de los diferentes barrios de Madrid.

## Dashboard

### Fuente de datos
Los archivos .csv se cargan como se hizo en la clase, como archivos de texto, y el archivo geojson se carga de manera especial como archivo espacial. A la hora de hacer las relaciones, el archivo principal de listing.csv y los otros dos se enlazan al archivo principal.

### Esquema de dashboard
El dashboard se divide en 3 partes: selección de propietario, selección de inmueble y analisis de reservas de cada inmueble. La idea del dashboard es hacer un análisis guiado, donde se va consiguiendo información a medida que profundizamos en los datos(Propietario-Inmueble-Datos)

#### Selección de propietario
En la primera parte, encontramos unos recuentos generales, de carácter numérico donde se contabilizan los datos de manera general, y posteriormente se puede seleccionar los diferentes propietarios, ordenados por volumen de ganancias. Si se desea, se puede filtrar por Barrio.

#### Selección de inmueble
Una vez seleccionado el propietario, podremos ver los datos generales de ese propietario, así como un listado de todos sus inmuebles. Se pueden filtrar por tipo de propiedad, para conseguir un listado mucho más restringido. Además podemos ver de manera visual donde se encuentran cada uno de los inmuebles.

#### Datos de inmueble
Una vez seleccionado el inmueble, podemos ver la información de reservas para los próximos 365 días, indicando el número de de días libre y ocupados que tenemos en cada mes.
