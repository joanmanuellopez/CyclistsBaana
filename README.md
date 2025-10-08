# Análisis de la serie temporal del recuento de paso de ciclistas por una estación de medida ubicada en la ciudad de Helsinki

## Contexto del proyecto
El objetivo de este proyecto es hacer una introducción al análisis de series temporales a partir del estudio de los datos obtenidos por una de las estaciones de medida de paso de ciclistas instaladas en la ciudad de Helsinki. Se dispone de las observaciones de esta estación medidora con intervalos de una hora en el periodo entre el 1 de enero de 2014 a las 00:00 hasta el 31 de diciembre de 2022 a las 23:00.

El principal objetivo de este proyecto es practicar el análisis de series temporales, en lenguaje Python, a partir del estudio de los datos obtenidos por una de las estaciones de medida de paso de ciclistas instaladas en la ciudad de Helsinki entre los años 2014 y y 2022. La estación de conteo elegida es la ubicada en la infraestructura denominada Baana, una antigua vía ferroviaria completamente segregada del tráfico de vehículos a motor que atraviesa el centro de la ciudad, acondicionada como corredor exclusivo para peatones y ciclistas. Se ha elegido esta estación por ser una de las que más pasos de ciclistas contabilizan.

Con el análisis exploratorio y las gráficas generadas se pretende dar resupesta a dos cuestiones:

* ¿Qué meses del año hay mayor paso de ciclistas por esta infraestructura?
* ¿Cuál es la tendencia en cuanto al uso anual de esta infraestructura?

### Retos
Una cuestión importante que hay que tener en cuenta a la hora de analizar los datos obtenidos es la precisión temporal. El intervalo de medida de los datos originales es de una hora, pero para responder a las preguntas planteadas es más que suficiente tener en cuenta los datos mes a mes. Por tanto, antes de iniciar el análisis, se debe hacer un paso previo para obtener una medida a escala mensual, en este caso el número medio de ciclistas contados por día en cada mes del periodo.

### Fuente de datos
Los datos que se han utilizado en este proyecto pertenece al Departamento de Desarrollo Urbano del Ayuntamiento de Helsinki y se ha descargado a través del portal de datos abiertos Avoin Data que lo publica bajo licencia CC-BY 4.0 (*). En concreto se dispone de las observaciones en intervalos de una hora, desde el día 1 de enero de 2014 a las 0:00 hasta el 31 de diciembre de 2022 a las 23:00. El dataset actualizado se puede encontrar en el siguiente enlace: [Number of Cyclists in Helsinki](https://www.avoindata.fi/data/en_GB/dataset/helsingin-pyorailijamaarat)

(*) *Licencia: [Helsingin pyöräilijämäärät](https://www.avoindata.fi/data/en_GB/dataset/helsingin-pyorailijamaarat) by [Helsingin kaupunkiympäristön toimiala](https://www.avoindata.fi/data/en_GB/organization/helsingin-kaupunkiympariston-toimiala) is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).*

## Conclusiones principales
La representación gráfica de los datos agregados mensualmente permiten observar algunos patrones en el uso de la bicicleta:
* Grandes diferencias en el conteo entre los meses de verano y los de invierno
* Descenso en el conteo en los meses de julio, posiblemente debido al periodo vacacional en la ciudad de Helsinki.

## Descripción del notebook de Jupyter incluidos
**timeseries_baana.ipynb**  
Único notebook usado para el desarrollo de este proyecto, se estructura en tres partes principales:
1. Carga de los datos y Análisis Exploratorio
2. Visualización de la evolución temporal del recuento de ciclistas
3. Descomposición de la serie temporal
