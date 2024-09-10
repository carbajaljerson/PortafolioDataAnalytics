
![GitHub repo size](https://img.shields.io/github/repo-size/scottydocs/README-template.md)
![GitHub contributors](https://img.shields.io/github/contributors/scottydocs/README-template.md)
[![HitCount](https://hits.dwyl.com/dwyl/hits.svg)](https://github.com/carbajaljerson/PI02_SiniestrosViales_CABA/)
![GitHub stars](https://img.shields.io/github/stars/scottydocs/README-template.md?style=social)


# <h1 align="center">**`Siniestros Viales en la Ciudad Atónoma de Buenos Aires (CABA)`**</h1>

Bienvenidos a continuación se presenta el desarrollo del Proyecto Individual de Análisis de Datos

## Introducción


El presente proyecto se desarrolló bajo el perfil de un Data Analyst y tiene como finalidad la elaboración de un proyecto de análisis de datos para obtener información y conocimiento, este requerimiento es solicitado por el Observatorio de Movilidad y Seguridad Vial (OMSV), que es un centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA). La realización del proyecto permitirá a las autoridades locales tomar decisiones claves para mitigar la cantidad de víctimas mortales en los siniestros viales en la Ciudad Atónoma de Buenos Aires (CABA).


Se llevó a cabo el análisis de los datos sobre los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, ocurridos entre los años 2016 y 2021. En este proyecto, compartiré mis hallazgos y brindaré recomendaciones a partir de  la identificación de patrones y tendencias.


## Contexto
Las muertes por siniestros viales en Argentina poseen cifras alarmantes los informes del Sistema Nacional de Información Criminal (SNIC), revelan que entre los años 2018 y 2022 se registraron 19630 muertes en siniestros viales en todo el país, estas cifras equivalen a un promedio de 11 víctimas fatales por día por accidentes de tránsito.

Esta es una gran problemática que afecta a todas las provincias, si bien algunas se ven más afectadas que otras, sigue siendo un factor que da que hablar en cada territorio. Al 2022 los siniestros totales que suceden en la provincia de Buenos Aires representan el 30%. Los siniestros viales involucran a diversos tipos de vehículos y actores en las vías públicas, y estos son automóviles, motos, bicicletas, peatones, atropellos, vehículos de carga y pasajeros. 

En el 2022, el número de muertes por accidentes de tránsito alcanzó a 3828 muertes fatales. Los expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.


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

Una vez que los datos están limpios, es importante revisar las relaciones que existen entre las variables de los datasets, identificar la presencia de outliers o anomalías (que no tienen que ser errores necesariamente), y verificar si existen patrones o conocimientos que sirvan en un análisis posterior. Una gráfica representativa de este proceso es la nube de palabras, que muestra cuales son las palabras que aparecen con una mayor frecuencia. A continuación se muestra la gráfica sobre las direcciones y se observa que la Avenida Gral Paz aparece con mayor frecuencia en los siniestros viales.

<p align="center" >
<img src="src\analisis08.png"  height=590 weight=580>
</p>
</br>
Por medio de los gráficos anteriores podemos identificar el rango de edad de 20 a 40 años y la franja horaria entre las 5 a 10 a.m. estan asociados a una mayor cantidad de Siniestros Viales, así como también se puede reconocer que el número más frecuente de víctimas es 1.  
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
Se observa que la mayor cantidad de siniestros viales ocurren al este de la Ciudad Autónoma de Buenos Aires, principalmente en las comunas 1 y 4.

## **3. Análisis de Datos**
- Los tres principales vehículos y/o medios de transporte asociados a un mayor número de víctimas son las motos, seguidas por los autos y las bicicletas. Las motos causaron casi la mitad de las muertes, representando el 42%. Esto resalta la importancia de abordar factores como el comportamiento del conductor, la infraestructura vial y las medidas de seguridad para las motos, así como el uso de cascos certificados, con el fin de reducir la mortalidad en los accidentes.

</br>
<p align="center" >
<img src="src\analisis.png"  height=450 weight=550>
</p>
</br>

- La mayor parte de los accidentes ocurrieron en las comunas 1, 4 y 9, por lo que estas áreas requieren una mayor atención para mejorar las medidas de seguridad vial. Factores como la alta densidad de población, el elevado volumen de tráfico, las redes de carreteras complejas y la interacción de diversos modos de transporte en estas comunas podrían estar contribuyendo al aumento de los accidentes de tránsito

<p align="center">
<img src="src\analisis02.png" height=250 weight=350>
</p>

- El grupo etario con mayor incidencia en los accidentes es el de 18 a 35 años. Dado que se trata de una muestra joven, es necesario considerar que factores como el aumento de velocidad y las distracciones en la carretera, pueden contribuir a una mayor frecuencia de accidentes.

<p align="center">
<img src="src\analisis03.png" height=300 weight=400>
</p>

- En el siguiente mapa se localizan los puntos donde ocurrieron los accidentes lo cual es de gran utilidad para identificar las principales zonas con un mayor número de víctimas. Esto ayuda a reconocer las avenidas relacionadas a los siniestros y, con base en esta información, se deben implementar políticas urbanas para mitigar la tasa de mortalidad por siniestros viales.


<p align="center">
<img src="src\analisis04.png" height=250 weight=350>
</p>

- Los Lunes y Sábados son los días que presentan un mayor número de víctimas, los meses con mayor frecuencia de siniestros son Noviembre y Diciembre. En cuanto a la franja horaria, las horas entre 5-7 a.m. estan asociadas a un mayor número de víctimas.

<p align="center">
<img src="src\analisis07.png" height=500 weight=600>
</p>


- El sexo Masculino está asociado a un mayor porcentaje de siniestros viales,representando el 76%, y el rango etario predominante es de 18 a 35 años. En el caso del sexo femenino, se observa que, cuando la edad supera los 55 años y la franja horaria es de 9 a 15 horas, también hay un aumento en el número de víctimas.

<p align="center">
<img src="src\analisis06.png" height=400 weight=550>
</p>


## **4. Creación de KPIs**

*  *Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.*  

La **tasa de homicidios en siniestros viales** está definida como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. <br>Su fórmula es: 
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
 
✅ Entre 2016 al 2018, se evidenció un aunmento significativo en la cantidad de siniestros viales. Sin embargo en los años posteriores, esta tendencia comenzó a reducirse (2019-2021). Se verificó que las motos son los vehiculos con mayor participación en los accidentes, así como el rango de edad comprendido entre 18 y 35 años.  
  
✅ La comuna 1, tiene asociada la mayor concentración de accidentes y son las avenidas "9 de Julio" y "Paseo Colón" las que registran un mayor número de víctimas.

✅ El rango de edad de las víctimas varián según al sexo: en los hombres, se sitúa entre los 18 y 35 años mientras que en las mujeres la edad es superior a los 55 años.

✅ El rol de la víctima que está relacionado a una mayor cantidad de accidentes es el Conductor, en comparación con el pasajero acompañante.
 
✅ El accidente típico ocurre un Sábado a las 7 horas en el mes de Diciembre. 


## **7. Recomendaciones**

- Se debe de generar campañas de concientización en las comunas que tienen un alto número de víctimas.
- Eliminar la contaminación visual en las principales avenidas, ya que esto aumenta la distracción de los conductores.
- Realizar campañas respecto a la seguridad vial hacia el sexo masculino sobre el rango de edad de 18 a 35 años y en mujeres que tienen una edad superior a 55 años.
- Debe existir un reglamento más riguroso para la obtención de la licencia de vehículos,  así como establecer un control en el uso obligatorio de casco certificado.
- Reforzar la seguridad vial por medio de operativos policiales en las principales avenidas, especificamente en el mes de Diciembre.


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
