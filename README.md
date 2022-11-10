![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# **PROYECTO INDIVIDUAL Nº3**

# <h1 align="center">**`Accidentes aéreos`**</h1>



## **Introducción**
Se realiza el siguiente informe para la  **Organización de Aviación Civil Internacional (OACI)**, organismo de la Organización de las Naciones Unidas, sobre los accidentes aéreos desde inicios del siglo XX. 


## **EDA**

Utilizando pandas, se realizó la importación del archivo csv con los datos de accidentes aéreos a trabajar.
Al hacer un análisis exploratorio se encontró que los valores faltantes contenían el caracter "?". Se remplazó por NaN.
Por otro lado, dicho archivo se encontraba con nombres de columnas poco ortodoxos, por lo que se procedió a cambiar el nombre de algunas y el tipo de dato que éstas contenían. Se procedió también a eliminar las siguientes columnas que luego no serían usadas en el análisis: "HORA declarada" y "summary". Las columnas resultantes fueros estas:

ID                      int64       Id del accidente
Ruta                    object      Ruta del vuelo
Operador                object      Operador
flight_no               object      Número de vuelo
route                   object      Ruta del vuelo
ac_type                 object      Tipo de aeronave
registration            object      Matricula
cn_ln                   object      
all_aboard              Int64       Total de personas abordo
passenger_aboard        Int64       Pasajeros a bordo
crew_aboard             Int64       Tripulación a bordo
cantidad de fallecidos  Int64       Total de fallecidos
passenger_fatalities    Int64       Pasajeros fallecidos
crew_fatalities         Int64       Tripulantes fallecidos
ground_fatalities       Int64       Fallecidos en tierra
date                    object      Fecha







