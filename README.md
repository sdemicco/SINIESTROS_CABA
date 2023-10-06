# SINIESTROS_CABA
Análisis de siniestros viales con victimas fatales en CABA
***
# Análisis de siniestros viales con victimas fatales en CABA

La cantidad de muertes causadas por accidentes de tránsito en Argentina es un asunto de gran interés que requiere un esfuerzo continuo para su mejora. Expertos en seguridad vial señalan que en Argentina, la probabilidad de que una persona pierda la vida en un accidente de tráfico es dos o incluso tres veces mayor que en un incidente de inseguridad delictiva. Esta estadística subraya la importancia de abordar de manera efectiva la seguridad vial y asignar recursos de manera adecuada para reducir los siniestros viales.

Para tomar decisiones efectivas en este campo, es fundamental contar con un sólido análisis de datos. El acceso y la interpretación de información precisa sobre los siniestros viales y sus causas son elementos esenciales para diseñar estrategias y políticas de seguridad vial efectivas que puedan contribuir a la reducción de estos incidentes.

En este contexto, mi labor se centró en la elaboración de un proyecto de anális de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales en CABA. 

### 1.	Fuente de Datos:
***
Datos públicos generados, guardados y publicados por el Gobierno de la Ciudad de Buenos Aires. <br>

> Dataset principal:<br>
- Archivo ‘Homicidios (XLSX)’:
Información sobre Homicidios y Lesiones en siniestros viales ocurridos en la Ciudad.
https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales
 
>Datasets complementarios: 
-	Conteo Vehicular.csv: 
Información de conteo sobre el paso de vehículos en diferentes cruces de calles de la Ciudad.
https://data.buenosaires.gob.ar/dataset/conteo-vehicular
- Barrios.csv:
Límites y ubicación geográfica de los barrios de la Ciudad.<br>
https://data.buenosaires.gob.ar/dataset/barrios
***

### 2.	Analisis exploratorio de datos:
 ![NumPy Badge](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=fff&style=for-the-badge)
 ![VSCODE](https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)
 ![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)
 ![Pandas](	https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
 ![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
 <br>

Los datos de Homicidios viales tenían una buena calidad, no presentaban valores duplicados ni nulos. Contenían una categoría SD para los registros ‘sin dato’, los cuales representaban una proporción muy baja respecto a la totalidad de datos. En algunos casos se pudieron corregir valores utilizando la información de datos de otras columnas.
Se eliminaron del conjunto de datos las columnas que no aportaban valor al análisis, ya sea por presentar pocos valores o información redundante. 
Se utilizó el dataset barrios.csv para poder asignarle el barrio a cada dirección de accidente y poder trabajar a nivel un poco más detallado que la comuna.
El análisis de las variables categóricas se realizó a partir de gráficos de frecuencia pudiendo encontrarse algunas relaciones importantes:
  * En las avenidas ocurren la mayor cantidad de accidentes fatales.
  * El Barrio Flores presenta una cantidad de accidentes fatales superior al resto de los barrios de CABA.
  * Las principales víctimas son los motociclistas, seguido por los peatones.
  * Los principales acusado son los autos,  seguidos por los  vehículos de transporte de pasajeros y luego transporte de cargas.
  * Hay  una tendencia de baja de accidentes fatales con los años.
  * El mes de diciembre presenta la mayor cantidad de accidentes fatales.
  * El rol de las victimas predominante es el del conductor seguido por peatón.
  * El sexo masculino prevalece sobre el femenino en las vitimas fatales.


### 3. Proyecto de Analisis de datos
![Power BI Badge](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=000&style=for-the-badge)
***
#### PARTE 1:
***
Esta sección cuenta con información de tendencia de homicidios en el tiempo, ubicación homicidios, tipo de calle, día de la semana y rango horario de los homicidios y el seguimiento del siguiente KPI:

**Reducción en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior**

*nota: Definimos a la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000*

En el gráfico de homicidios por semestre, se observa una tendencia de reducción de accidentes desde el 2016 al 2021. Es importante mencionar que durante el periodo estudiado, durante 2020 ocurrió la pandemia por COVID. Durante ese año bajo fuertemente la circulación de personas en la ciudad , tanto peatones como motorizadas. Luego en 2021, la situación no vuelve a ser la misma que pre_pandemia ya que se instala el hábito del trabajo home-office. 

![Evolucion de victimas con el tiempo](assets/cantidad_de_victimas.png)


El Barrio de Flores presentó la mayor cantidad de accidentes ocurridos en los últimos 3 años, seguido por los barrios de Palermo y Balvanera y Belgrano
En Flores y Palermo el porcentaje de ocurrencia estos accidentes en Avenidas es superior al 95%. En cambio este porcentaje disminuye a un 50% para los Barrios de Balvanera y Belgrano. 
Con respecto al horario de ocurrencia de accidentes, se observa que en horario entre los 7 a 9 hs ocurren más accidentes que en el resto de los horarios, lo cual puede estar asociado ser hora de circulación pico.

Un punto a tener en cuenta es que si bien el Barrio Flores posee la mayor cantidad de accidentes en el periodo estudiado, también muestra un fuerte decrecimiento de los mismos a partir del segundo trimestre del año 2018.  Analizando particularmente a las victimas peatones, se puede notar que Flores pasó de ser el Barrio con mayor cantidad de homicidios de peatones en los años de 2016, 2017 q 2018 a no tener víctimas peatones en 2021. Esta tendencia es previa a la pandemia. Por lo tanto es recomendable estudiar las medidas que se tomaron en dicho Barrio y replicarlas en otras zonas. 
- Cantidad de victimas en barrio Flores<br>
![Evolucion de victimas por accidente BARRIO Flores](assets/cantidad_victimas_flores.png)<br>
- Cantidad de victimas peatones en barrio Flores <br>
![Evolucion de victimas por accidente de peatones BARRIO Flores](assets/cantidad_peatones_flores.png)

El KPI de reducción de tasa de accidentes viales semestral es ampliamente superado. El KPI objetivo es de un 10% de reducción y se tiene un valor de 23,64%.
<br>
<p align="center">
<img src="assets/KPI_1.png" alt="Texto alternativo" width="250" height="160" /> 
 <br>

***
#### PARTE 2: 
***

Esta sección cuenta con información de  gráficos de evolución de cantidad de muertes discriminado por tipo de víctima (moto, peatón, etc).  También se muestra el tipo de vehículo acusado en el siniestro. Finalmente se complementa el análisis con información de las victimas tal como el sexo y el rango etario.<br>
<br>
Se reliza el seguimiento del indicador de rendimiento clave, KIP definido como :<br>
**Reducción de en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior**<br>
<br>
*nota: Definimos a la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100* <br>
<br>
Las principales víctimas fatales de accidentes de tránsito son los peatones y  motociclistas. En tercer puesto se encuentran los autos. Se observa que esta relación se mantuvo en todo el periodo estudiado.
<br>
<p align="center">
<img src="assets/muertes_tipo_victima.png" alt="victimas_tipo" width="450" height="360" /> 
 <br>
 
Al analizar cada categoría por separado puse observarse que hay una tendencia a la baja de accidentes de tránsito para todas las categorías de victimas pero es más marcada en los peatones. <br>
En el caso de las victimas motociclistas la tendencia general es de baja en el periodo 2016-2021. Sin embargo en el último año hubo una tendencia de subida. Este comportamiento pude verse reflejado en el no cumplimiento del KPI el cual muestra que hubo un incremento relativo de un 64,29% de victimas de moto en 2021 respecto al año 2020.  

<p align="center">
<img src="assets/KPI_2.png" alt="Texto alternativo" width="230" height="160" /> 
 <br>


Esto es esperable ya que  la cantidad de víctimas en 2020 se vio afectada por la disminución abrupta de circulación en las calles por motivo de la pandemia.
Teniendo en cuenta todo el periodo de datos analizado, se observa que predominan las victimas de sexo masculino, representando un 87% de total de víctimas.<br> 


Este porcentaje se ve reducido para as victimas peatones que posee un porcentaje más equilibrado entre sexos del 61%.  Esto puede tener origen en que la proporción de hombres circulando en autos y motos es superior a la de mujeres. No ocurre los mismo con los peatones. 

Finalmente se observa que el top 3 de vehículos acusados de cometer homicidios son autos, transporte de pasajeros y transporte de cargas.
Es importante destacar que la cantidad de accidentes muertes por Autos es similiar a la de los colectivos y transporte de cargas.  Sin embargo las proporciones entre estos vehículos es muy diferente, de este análisis surge el tercer KPI.

***
#### PARTE 3: 
***
En esta sección del informe se trabaja en la definición de un tercer KPI que busca establecer un objetivo sobre la cantidad de muertes causadas  por tipo de vehículo en relación a la cantidad total de vehículos que circulan de este tipo.<br> 
<br>
Por ejemplo en análisis anteriores vimos que la cantidad absoluta de muertes provocadas  por autos fue de 204,  de colectivos 172 y 146 por transporte de cargas. Se encuentran todas en el mismo orden de magnitud.
Sin embargo la cantidad de autos que circulan es diferente a los colectivos y camiones de carga.<br> 
<br>
Para poder abordar este análisis se utilizó el dataset que contiene información de conteo de tipo vehículos en diferentes cruces de calles en CABA, en los años 2018 y 2019.  

<p align="center">
<img src="assets/puntos_conteo.png" alt="conteo" width="600" height="200" /> 
 <br>

Promediando todos los puntos de medición y los años se obtiene que la cantidad de autos por colectivo es de 24,42, mientras la cantidad de autos por camion de carga es de 172.<br>
<br>
De este primer análisis se desprende que la cantidad de colectivos y camiones que generan muertes con relación a sus totales circulando es significativamente mayor a la de autos.
<br>
<br>
Se define el siguiente KPI para seguimiento:<br>
<br>
**Reducción del 30% del índice_colectivo_auto (C_A_index):**<br>
Donde el indice colectivos_autos (C_A_index) se define como:<br>
C_A_index =  tasa de accidentes de colectivos/la tasa de accidentes de autos.  
*Tasa de accidentes de autos= accidentes causados por autos/ total autos.<br>*
*Tasa de accidentes de colectivos= accidentes causados por colectivos/ total colectivos.*<br>
<br>
En el siguiente gráfico se muestra la evolución de C_A_index en el preíodo estudiado.
El valor promedio de C_A_index en todo el periodo es aproximadamente 20, lo cual indicaria que la canitdad de muertes por colectivos sobre el total de colectivos es 20 veces mayor a la cantidad de muertes que genera un auto sobre el total de autos circulando.
Este analisis presenta un fuerte punto de focalizacion de esfuerzo de mejora direccinado al transporte de pasajeros. 
<p align="center">
<img src="assets/evolución_c_a_index.png" alt="c_a_index" width="600" height="200" /> 
 <br>

Este indice presenta una tendencia de baja con el tiempo y puede observarse que el procentaje de reducción del C_A_index tomo un valor de 35% superando el valor de 30% propuesto.

<p align="center">
<img src="assets/KPI_c_a_index.png" alt="kpi_c_a_index" width="230" height="160" /> 
 <br>

### Conclusiones
***
