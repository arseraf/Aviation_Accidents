![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# **PROYECTO INDIVIDUAL Nº3**

# <h1 align="center">**`Accidentes aéreos`**</h1>



## **Introducción**
Se realiza el siguiente informe para la  **Organización de Aviación Civil Internacional (OACI)**, organismo de la Organización de las Naciones Unidas, sobre los accidentes aéreos desde inicios del siglo XX. 


## **EDA**

Utilizando pandas, se realizó la importación del archivo csv provisto con los datos de accidentes aéreos a trabajar.
Al hacer un análisis exploratorio se encontró que los valores faltantes contenían el caracter "?". Se remplazó por NaN.
Por otro lado, dicho archivo se encontraba con nombres de columnas poco ortodoxos, por lo que se procedió a cambiar el nombre de algunas y el tipo de dato que éstas contenían. Se procedió también a eliminar las siguientes columnas que luego no serían usadas en el análisis: "HORA declarada" (dato que no resulta relevante para nuestro análisis) y "summary", columna que contiene información detallada del accidente pero el extraer su información excedía los alcances de este proyecto. Las columnas resultantes fueron las detalladas a continuación:

- ID:                      (int64)       Id del accidente
- Ruta:                    (object)      Ruta del vuelo
- Operador:                (object)      Operador
- flight_no:               (object)      Número de vuelo
- route:                   (object)      Ruta del vuelo
- ac_type:                 (object)      Tipo de aeronave
- registration:            (object)      Matricula
- cn_ln:                   (object)      
- all_aboard:              (Int64)       Total de personas abordo
- passenger_aboard:        (Int64)       Pasajeros a bordo
- crew_aboard:             (Int64)       Tripulación a bordo
- cantidad de fallecidos:  (Int64)       Total de fallecidos
- passenger_fatalities:    (Int64)       Pasajeros fallecidos
- crew_fatalities:         (Int64)       Tripulantes fallecidos
- ground_fatalities:       (Int64)       Fallecidos en tierra
- date:                    (object)      Fecha

Adicionalmente, se utilizaron dos datasets donde se detalla la cantidad de vuelos y de pasajeros en los últimos 20 años. El único tratamiento que se le realizó a estos datasets fue eliminar las filas de los valores anuales totales y convertir a Int algunos valores que fueron importados como texto.

## **Database**

Se creó la base de datos en MySQL de manera local, realizando una tabla para cada dataset trabajado.

## **PowerBI**

Para realizar el dashboard, en primer lugar se importaron las tablas de MySQL. También se creó una tabla "calendario" con la cual se relacionaron todas las tablas. 
El objetivo del dashboard es visualizar los datos y ofrecer un apoyo visual a la presentación oral del proyecto. Permite definir periodos para evaluar fácilmente ciertas tendencias o sucesos.
También, es posible filtrar los resultados por tipo de actividad: militar, civil o comercial. Para ello, se definió como militar a aquellos registros que contenían la palabra "military" en la columna "operador". La categorización entre civil y comercial resultó más compleja: se considera como civil a las aeronaves con menos de 4 ocupantes y comercial con 4 o más. Este filtro no es ideal ya que muchos de los vuelos de carga (comerciales) cumplirían con la condición establecida para vuelos civiles.  Sin embargo, dado el alcance de este informe, se considera aceptable.






### Fuentes externas:

Base de datos de vuelos y pasajeros (periodo 2002-2020):
https://www.transtats.bts.gov/


