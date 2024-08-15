
![GitHub repo size](https://img.shields.io/github/repo-size/scottydocs/README-template.md)
![GitHub contributors](https://img.shields.io/github/contributors/scottydocs/README-template.md)
[![HitCount](https://hits.dwyl.com/dwyl/hits.svg)](https://github.com/carbajaljerson/PI02_SiniestrosViales_CABA/)
![GitHub stars](https://img.shields.io/github/stars/scottydocs/README-template.md?style=social)


# <h1 align="center">**`Siniestros Viales en la Ciudad Atónoma de Buenos Aires (CABA)`**</h1>

Bienvenidos a continuación se presenta el desarrollo del Proyecto Individual de Análisis de Datos

## Introducción


El presente proyecto se desarrolló bajo el perfil de un Data Analyst y tiene como finalidad la elaboración de un proyecto de análisis de datos para obtener información y conocimiento, este requerimiento es solicitado por el Observatorio de Movilidad y Seguridad Vial (OMSV), que es un centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA). La realización del proyecto permitirá a las autoridades locales tomar decisiones claves para mitigar la cantidad de víctimas mortales en los siniestros viales en la Ciudad Atónoma de Buenos Aires (CABA).


Mediante el análisis de los datos sobre los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, entre los años 2016 y 2021, descubrí varias observaciones que pueden guiar a la toma de decisiones futuras por las autoridades. En este proyecto, compartiré mis hallazgos y brindaré recomendaciones que estan basadas en información que han sido derivados de un dataset de homicidios en siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA).


## Contexto
Las muertes por siniestros viales en Argentina poseen cifras alarmantes los informes del Sistema Nacional de Información Criminal (SNIC), revelan que entre 2018 y 2022 se registraron 19'630 muertes en siniestros viales en todo el país.  Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito.

Esta es una gran problemática que afecta a todas las provincias, si bien algunas se ven más afectadas que otras, sigue siendo un factor que da que hablar en cada territorio. Al 2022 los siniestros totales que suceden en la provincia de Buenos Aires representan el 30%. Los siniestros viales involucran a diversos tipos de vehículos y actores en las vías públicas, y estos son automóviles, motos, bicicletas, peatones, atropellos, vehículos de carga y pasajeros. 

Solo en 2022, el número de muertes por accidentes de tránsito alcanzó a 3'828 muertes fatales. Los expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.


## 📊 Alcance del Proyecto

El siguiente proyecto contiene los siguientes desarrollos:

- Extracción Transformación y Carga sobre la data Hechos y de Victima
- Análisis Exploratorio de Datos
- Creación de Dashboard y Análisis con PowerBI
- Creación de KPIs

## Datos

Este proyecto se desarrolló en base al dataset denominado Homicidios, que se encuentra en formato de Excel y contiene dos hojas de datos :

- Hechos: contiene datos específicamente relacionados a los siniestros como lo son la fecha y hora del siniestro,  cantidad de víctimas, el lugar de hecho, la comuna, la dirección, la geolocalización, el tipo de víctima y los acusados.

- Víctimas: contiene datos relacionados con las víctimas y estos son la edad, el sexo, el rol, la fecha de fallecimiento, así como también la fecha del siniestro.

Los datos utilizados para este proyecto de análisis, estan en el siguiente [enlace de descarga](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales) 


## **DESARROLLO DEL PROYECTO ** :white_circle:

## **1. Etapa del proceso ETL** :

- Carga del archivo con extensión .xlsx con la libreria pandas.
- Luego se realizó el trabajo ETL(Extracción, Transformación y Carga) de las hojas de Hechos y de Víctimas.
- Se realizaron diversas transformaciones cumpliéndose con la estandarización de los datos se analizaron nulos y duplicados, se eliminaron columnas redundantes, entre otras tareas.
- Luego de las transformaciones y normalización de los datos se exportaron 2 archivos .csv de Hechos y Víctimas para realizar la respectiva carga las tablas en la Base de Datos de MySQl.


## **2. Análisis Exploratorio de los Datos (EDA)**

Una vez que los datos están limpios, es tiempo de revisar las relaciones que existen entre las variables de los datasets, encontrar si hay presencia de outliers o anomalías (que no tienen que ser errores necesariamente), y se verificó si hay algún patrón o conocimiento que sirva en un análisis posterior. Una gráfica muy representativa de este proceso es las nubes de palabras que nos mostrarán cuales son las palabras que se presentan con una mayor frecuencia, a continuación mostraremos la gráfica sobre la columna 'Dirección Normalizada' con lo cual se puede ver que las palabras 'gral paz' y 'av' representan avenidas y son las que aparecen con mayor frecuencia en los siniestros viales

<p align="center" >
<img src="src\analisis08.png"  height=590 weight=580>
</p>
</br>
Por medio de los gráficos anteriores podemos identificar el rango de edad de 20 a 40 años y la Franja Horaria de 5 a 10 estan asociados a una mayor cantidad de Siniestros Viales así como también se puede reconocer que el número más frecuente de víctimas es 1.  
</br>
<p align="center">
<img src="src\nube.png"  height=300 weight=400>
</p>
El mapa de calor nos ayuda a obtener una representación visual de los puntos de Localización de los Siniestros Viales en la Ciudad Autónoma de Buenos Aires (CABA) donde los colores más cálidos reflejan una mayor concentración de Siniestros, mientras que los colores frios indican un menor número de Siniestros.

</br>
<p align="center">
<img src="src\mapa.png"  height=300 weight=400>
</p>
</br>
Se reconoce que la mayor cantidad de Siniestros Viales se encuentran al Este de la Ciudad Autónoma de Buenos Aires y corresponden a las comunas 1 y 4

## **3. Análisis de Datos**
- Los tres principales vehículos y/o medios de transporte asociados a una mayor cantidad de víctimas son las motos, seguidos de los autos y bicicletas. Las motos causaron casí la mitad de la muertes representando el 42%. Esto pone de relieve el importante impacto y participación de las motos en los accidentes de tráfico; es crucial abordar factores como el comportamiento del conductor, la infraestructura vial y las medidas de seguridad de las motos como el uso de casco certificado para mitigar la mortandad en los accidentes.

</br>
<p align="center" >
<img src="src\analisis.png"  height=450 weight=550>
</p>
</br>

- La mayor parte de accidentes ocurrieron en las comunas 1, 4 y 9 ante esto es necesario indicar que estas comunas requieren una mayor atención para mejorar las medidas de seguridad vial. Factores como una mayor densidad de población, un mayor volumen de tráfico, redes de carreteras complejas y diversos modos de transporte que interactúan en estas comunas pueden estar contribuyendo al incremento de accidentes de tránsito.

<p align="center">
<img src="src\analisis02.png" height=250 weight=350>
</p>

- El rango de edades involucrado en la mayor cantidad de accidentes es el que está comprendido entre los 18 a 35 años de edad, al tratarse de una muestra joven se debe de tener en cuenta factores como el aumento de velocidad y las distracciones en la ruta pueden contribuir a una mayor incidencia de accidentes.

<p align="center">
<img src="src\analisis03.png" height=300 weight=400>
</p>

- En el siguiente mapa se localizan los puntos donde ocurrieron los accidentes nos sirve de mucha ayuda ya que nos muestra las principales zonas donde existe una mayor número de víctimas, esto ayuda a reconocer las avenidas relacionadas a los siniestros y a partir de esta información se debe de realizar políticas urbanas para lograr mitigar la tasa de mortandad por siniestros viales.


<p align="center">
<img src="src\analisis04.png" height=250 weight=350>
</p>

- Podemos identificar los días Lunes y Sábados son los que presentan un mayor número de víctimas, así como también los meses con mayor frecuencia de siniestros son los meses de Noviembre y Diciembre. Sobre la franja horaria podemos añadir que entre las horas 5-7 estan asociadas a un mayor número de víctimas.

<p align="center">
<img src="src\analisis07.png" height=500 weight=600>
</p>


- Se halló que el sexo Masculino es el que tiene asociado un mayor porcentaje en los siniestros viales con un 76% y rango de edad entre 18-35 años; con respecto al género femenino se verifica que cuando la edad supera los 55 años y la franja horaria es de 9-15 horas esta asociada a un mayor número de víctimas.  

<p align="center">
<img src="src\analisis06.png" height=400 weight=550>
</p>


## **4. Creación de KPIs**

* *Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior*
    la **tasa de homicidios en siniestros viales** está definida como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. <br>Su fórmula es: 
    (Número de homicidios en siniestros viales / Población total) * 100,000

<p align="center"><img src="src\kpi01.png" height=300 weight=400></p>
    En este caso, la tasa de homicidios en siniestros viales del Semestre 2020 respecto al semestre anterior del 2019 representa una mejor variación y esta por encima del objetivo del 10% alcanzando el objetivo propuesto con un 34%.

* *Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior*

    Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: <br>(Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

<p align="center"><img src="src\kpi02.png" height=340 weight=500></p>
    En este caso, el año 2020 respecto anterior del 2019 sobre el número de accidentes mortales en moto representa una mejor variación y esta por encima
    del objetivo del 7% alcanzando el objetivo propuesto con un 42%
    
* *Reducir en un 19% la cantidad de accidentes mortales en el último año, en CABA, respecto al año anterior*

    Su fórmula para medir la evolución de los accidentes mortales es: (Número de accidentes mortales en el año anterior - Número de accidentes mortales en el año actual) / (Número de accidentes mortales en el año anterior) * 100

<p align="center"><img src="src\kpi03.png" height=340 weight=450></p>
    En este caso, el año 2019 respecto anterior del 2018 sobre el número de accidentes mortales representa una mejor variación y esta por encima
    del objetivo del 19% alcanzando el objetivo propuesto con un 30%.

## **5. Dashboard**
El Dashboard desarrollado se encuentra en el siguiente enlace [Dashboard](https://tinyurl.com/2btuakma)

## **6. Conclusiones**

Mis principales conclusiones sobre la evolución de los accidentes de tráfico en CABA son los siguientes:
 
✅ Del 2016 al 2018 existe una mayor cantidad de siniestros viales en los años posteriores esta se fue reduciendo (2019-2021) y se verificó que son las motos las que tienen mayor participación en accidentes así como los rangos de edades entre 18-35 años.  
  
✅ La comuna 1, es la que tiene la mayor concentración de accidentes y se verico que las avenidas "9 de Julio" y "Paseo Colón" son las que tienen asociadas un número mayor de víctimas.

✅ El rango de edad de la víctima cuando el sexo es masculino está entre 18-35 años y cuando el sexo es femenino la edad es superior a 55 años.

✅ El rol de la víctima asociado a una mayor cantidad de accidentes es el Conductor en comparación con el pasajero acompañante.
 
✅ El accidente típico se produce un Sábado a las 7 horas en el mes de Diciembre. 


En función de lo anterior, se hacen las siguientes recomendaciones:

- Se debe de generar campañas de concientización en las comunas que tienen un alto número de víctimas; así como eliminar la contaminación visual en las principales avenidas ya que esto aumenta la distracción de los conductores.
- Realizar campañas respecto a la seguridad vial hacia el sexo masculino sobre el rango de edad de 18 a 35 años.
- Debe existir un reglamento más riguroso para la obtención de la licencia de vehículos y especificamente sobre quienes usan moto se debe establecer un control en el uso obligatorio de casco certificado.
- Es en el mes de Diciembre donde se debería reforzar la seguridad vial por medio de operativos policiales en las principales avenidas.


## 🛠 Tecnologías Utilizadas

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
