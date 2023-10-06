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

Los datos de Homicidios viales tenían una buena calidad, no presentaban valores duplicados ni nulos. Contenían una categoría SD para los registros ‘sin dato’, los cuales representaban una proporción muy baja respecto a la totalidad de datos. En algunos casos se pudieron corregir valores utilizando la información de datos de otras columnas.
Se eliminaron del conjunto de datos las columnas que no aportaban valor al análisis, ya sea por presentar pocos valores o información redundante. 
Se utilizó el dataset barrios.csv para poder asignarle el barrio a cada dirección de accidente y poder trabajar a nivel un poco más detallado que la comuna.
El análisis de las variables categóricas se realizó a partir de gráficos de frecuencia pudiendo encontrarse algunas relaciones importantes:
  * En las avenidas ocurren la mayor cantidad de accidentes fatales.
  * El Barrio Flores presenta una cantidad de accidentes fatales superior al resto de los barrios de CABA+
  * La mayor cantidad de homicidios se da para el choque entre vehículos de transporte de pasajeros y peatones.
  * Las principales víctimas son los motociclistas, seguido por los peatones.
  * Los principales acusado son los autos,  seguidos por los  vehículos de transporte de pasajeros y luego transporte de cargas.
  * Hay  una tendencia de baja de accidentes fatales con los años.
  * El mes de diciembre presenta la mayor cantidad de accidentes fatales.
  * El rol de las victimas predominante es el del conductor seguido por peatón.
  * El sexo masculino prevalece sobre el femenino en las vitimas fatales.


### Proyecto de Analisis de datos
***
El proyecto de análisis de datos puede dividirse en tres partes:
#### 1) PARTE 1: Información de tendencia de homicidios en el tiempo, ubicación homicidios, tipo de calle, día de la semana y rango horario de los homicidios. <br>
KPI_TASA_ACCIDENTES: Reducción en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.
Siendo: Tasa de homicidios en siniestros viales al número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso se toman 6 meses.

![graficos](URL_de_la_imagen)

En el gráfico de homicidios por semestre, se observa una tendencia de reducción de accidentes desde el 2016 al 2021. Es importante mencionar que durante el periodo estudiado, durante 2020 ocurrió la pandemia por COVID. Durante ese año bajo fuertemente la circulación de personas en la ciudad , tanto peatones como motorizadas. Luego en 2021, la situación no vuelve a ser la misma que pre_pandemia ya que se instala el hábito del trabajo home-office. 


![graficos](URL_de_la_imagen)










### Conclusiones
***
