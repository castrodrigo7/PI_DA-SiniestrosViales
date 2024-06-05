

## Proyecto Individual - Análisis de Siniestros Viales en CABA con Víctimas Fatales (2016-2021)

### Introducción ⚠️ 🚧
Este proyecto se realizó simulando el papel de un Data Analyst, con la finalidad de elaborar un análisis de datos solicitado por el Observatorio de Movilidad y Seguridad Vial (OMSV), bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA). El objetivo del proyecto es proporcionar información fundamentada para la toma de decisiones, destinada a la prevención y reducción de siniestros viales con víctimas fatales en la Ciudad de Buenos Aires.

Las tasas de mortalidad relacionadas con siniestros viales son un indicador crítico de la seguridad vial en una región. Estas tasas se calculan generalmente como el número de muertes por cada cierto número de habitantes o vehículos registrados. Reducir estas tasas es un objetivo clave para mejorar la seguridad vial y proteger vidas en la ciudad.

Para este proyecto, se utilizaron datos públicos de un dataset sobre homicidios de siniestros viales en la Ciudad de Buenos Aires durante los años 2016-2021, disponibles en la página oficial de CABA.

### Contexto ⚠️ 🚧
Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos. Estos incidentes pueden resultar en daños materiales, lesiones graves o fatales para los involucrados.

En Argentina, cada año mueren cerca de 4,000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, sigue siendo la principal causa de muertes violentas en el país. Informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19,630 muertes en siniestros viales en todo el país, lo que equivale a 11 personas por día.

Buenos Aires es la capital y ciudad más poblada de la República Argentina, con una superficie superior a los 200 km² y un perímetro de 60 km. Los habitantes se distribuyen en barrios que, desde el punto de vista político-administrativo, se agrupan en quince comunas. La densidad de población supera los 15,000 habitantes por kilómetro cuadrado, siendo las zonas centro y norte las más densamente pobladas. Según el Censo de 2022, la población de la ciudad es de 3,120,612 habitantes. Solo en 2022, se contabilizaron 3,828 muertes fatales en siniestros viales. Expertos indican que en Argentina la probabilidad de morir en un siniestro vial es dos o tres veces mayor que en un hecho de inseguridad delictiva.

Dado este contexto, el estudio del problema para la prevención y disminución de siniestros viales es esencial para las autoridades.

### Tecnologías Utilizadas

El proyecto hace uso de diversas tecnologías y herramientas para realizar un análisis exhaustivo de los siniestros viales. Algunas de las principales tecnologías utilizadas incluyen:

- [![Visual Studio Code](https://img.shields.io/badge/IDE-Visual%20Studio%20Code-blue)](https://code.visualstudio.com/)
- [![Python](https://img.shields.io/badge/-Python-333333?style=flat&logo=python)]
- [![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)](https://jupyter.org/)
- [![Pandas](https://img.shields.io/badge/Library-Pandas-brightgreen)](https://pandas.pydata.org/)
- [![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-blue)](https://matplotlib.org/)
- [![Seaborn](https://img.shields.io/badge/Library-Seaborn-yellow)](https://seaborn.pydata.org/)
- [![Power BI](https://img.shields.io/badge/BI%20Tool-Power%20BI-yellow)](https://powerbi.microsoft.com/)

### Desarrollo ⚠️ 🚧

#### Datos ⛔
Para este proyecto se trabajó con la base de datos de Víctimas Fatales en Siniestros Viales en formato Excel, que contiene dos pestañas de datos:

- **HECHOS:** Incluye una fila por cada hecho con un id único y variables temporales, espaciales y participantes asociadas.
- **VICTIMAS:** Contiene una fila por cada víctima, con variables de edad, sexo y modo de desplazamiento asociadas, vinculadas a los HECHOS mediante el id del hecho.

**Análisis exploratorio de datos (EDA)**

El mismo consiste en los siguientes pasos: 

1. **Ingesta de datos**: se importan librerias y se leen los datos a trabajar. 

2. **Inspección preliminar**: se analiza el dataset correspondiente con el objetivo de interpretar que información tenemos, la calidad de sus datos, entre otras cosas. 

3. **Duplicados**: se busca la existencia de registros duplicados y se decide que hacer con ellos. 

4. **Valores faltantes**: al igual que con los duplicados, buscamos valores faltantes y determianamos como vamos a trabajar con ellos. 

5. **Outliers**: se rastrea dentro de los datasets, la posible existencia de outliers con el objetivo de eliminarlos si fuera necesario y que eso no altere la calidad del análisis. 

6. **Gráficos (variables cualitativas)**: de las misma manera que con las variables cuantitativas, analizamos las variables categóricas con el mismo objetivo que el anterior. 

7. **Gráficos (variables cuantitativas)**: se identifican las variables numéricas y se busca correlación entre ellas para evitar sesgamientos e inconsistencias. Además, se analiza la distribución de las mismas mediante la utilización de gráficos con el objetivo de identificar tendencias y comportamientos en los datos que puedan ser de utilidad para el análisis posterior y la creación del dashboard. 

#### Análisis de los Datos ⛔

##### Análisis Temporal y Participativo:

- **Vehículos Involucrados:** Los autos, colectivos y vehículos de carga fueron los principales acusados en los siniestros. Las víctimas, en su mayoría, eran conductores o peatones, con motociclistas y peatones como los más afectados.
- **Roles de las Víctimas:** Las víctimas masculinas eran predominantemente conductores, mientras que las víctimas femeninas incluían tanto conductores como peatones.
- **Tendencias Anuales:** Los accidentes con víctimas fatales mostraron una tendencia alta y estacionaria entre 2016 y 2018, que luego se volvió bajista, influenciada por la pandemia de COVID-19 en 2020. Hubo un pico de siniestros en diciembre de 2021 antes de retomar la tendencia bajista.
- **Meses Críticos:** Diciembre (86 víctimas) y agosto (71 víctimas) registraron las mayores cantidades de víctimas fatales.
- **Días de la Semana:** Los sábados y domingos fueron los días con mayor número de víctimas fatales, con 114 víctimas cada uno.
- **Horarios Críticos:** Los siniestros viales se concentraron en los horarios de ingreso laboral (5-9h), almuerzo (12-14h) y salida del trabajo (17-18h). Durante los fines de semana, los horarios críticos fueron las salidas nocturnas (4-7h).

##### Análisis Demográfico y Geográfico:

- **Edad de las Víctimas:** La mayoría de las víctimas masculinas se encontraban en el rango etario de 20-40 años, mientras que las víctimas femeninas estaban en los rangos de 40-60 y 80 años.
- **Correlación Edad y Hora:** Los siniestros protagonizados por hombres ocurrían mayormente en horarios de ingreso y egreso laboral, mientras que los accidentes que involucraban a mujeres eran más comunes cerca del horario de almuerzo.
- **Distribución Geográfica:** Utilizando los datos de las comunas de CABA, se identificó que las comunas con más siniestros fueron las 1, 4, 9, 8 y 7.
- **Tipos de Vía:** El 62% de los siniestros ocurrieron en avenidas y el 82% en cruces entre calles, mostrando un patrón consistente a lo largo de los años.


### Indicadores de Rendimiento Clave (KPI) 🚦

#### 1. Reducir en un 10% la tasa de homicidios en siniestros viales en los últimos seis meses en comparación con el semestre anterior

- **Definición:** Tasa de homicidios en siniestros viales se refiere al número de víctimas fatales por accidentes de tránsito por cada 100,000 habitantes en una región y tiempo específico.
- **Fórmula:** (Número de homicidios en siniestros viales / Población total) * 100,000.
- **Interpretación:** Si el KPI es mayor que 0, indica una reducción de homicidios en comparación con el semestre anterior. Una reducción mayor al 10% significa que el objetivo está cumplido.

#### 2. Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año en comparación con el año anterior

- **Definición:** Cantidad de accidentes mortales de motociclistas se refiere al número absoluto de accidentes fatales que involucraron a motociclistas en un período específico.
- **Fórmula:** (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / Número de accidentes mortales con víctimas en moto en el año anterior * 100.
- **Interpretación:** Si el KPI es mayor que 0, indica una reducción en los accidentes mortales de motociclistas en comparación con el año anterior. Una reducción mayor al 7% significa que el objetivo está cumplido.

#### 3. Reducir en un 15% los accidentes mortales en avenidas en los últimos seis meses en comparación con el semestre anterior

- **Definición:** Cantidad de accidentes mortales en avenidas se refiere al número absoluto de accidentes fatales que ocurrieron en avenidas en un período específico.
- **Fórmula:** (Número de accidentes mortales con víctimas en avenidas en el semestre anterior - Número de accidentes mortales con víctimas en avenidas en el semestre actual) / Número de accidentes mortales con víctimas en avenidas en el semestre anterior * 100.
- **Interpretación:** Si el KPI es mayor que 0, indica una reducción en los accidentes mortales en avenidas en comparación con el semestre anterior. Una reducción mayor al 15% significa que el objetivo está cumplido.


### Conclusiones ⚠️ 🚧
A partir del análisis exhaustivo de los datos y su posterior visualización a través de un dashboard en PowerBi, se concluye que:

- Entre 2016 y 2021, hubo 717 víctimas fatales por siniestros de tránsito en CABA.
- Las franjas horarias de mayor riesgo son la de ingreso laboral (5-9h), almuerzo (12-14h) y regreso a casa (17-18h), con un aumento en los fines de semana durante las horas de salidas nocturnas (3-7h).
- Las víctimas son mayoritariamente masculinas (76%), en el rango etario de 20-40 años. Los siniestros en que están involucrados los hombres ocurren principalmente durante los horarios laborales y las noches de fines de semana.
- Los siniestros se concentran en avenidas y cruces de calles, con las comunas 1 y 4 registrando los mayores números de accidentes.
- Los vehículos más frecuentemente involucrados como responsables son autos, colectivos y vehículos de carga, mientras que las víctimas son principalmente motociclistas y peatones.

Para reducir la cantidad de siniestros viales con víctimas fatales, se recomienda:

- **Mejorar las señales y controles en avenidas, especialmente en las comunas 1 y 4.
- **Implementar campañas de prevención dirigidas a hombres de 20-40 años, enfocadas en los horarios de mayor riesgo.
- **Fortalecer la educación y concienciación vial, especialmente en horarios críticos y en zonas de alto tráfico peatonal y de motociclistas.
- **Revisar y mejorar la infraestructura vial en las avenidas y cruces más peligrosos, para facilitar un tránsito más seguro.