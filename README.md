# Proyecto Integrador - Modulo 5
Este proyecto se ha realizado en equipo por:
* Leandro Funes
* Jay Peralta

Alumnos de la Cohorte 21 de Data Science de [Henry](https://www.soyhenry.com/)

## Índice

1. [Introducción](#introducción)
2. [Descripción del dataset](#descripción-del-dataset)
3. [EDA y ETL](#eda-y-etl)
4. [Descripción del Análisis Exploratorio de los Datos](#descripción-del-análisis-exploratorio-de-los-datos)
5. [Preguntas](#preguntas)
   - [1) ¿Qué podemos describir con los datasets acerca del negocio de Airbnb?](#1-¿qué-podemos-describir-con-los-datasets-acerca-del-negocio-de-airbnb)
   - [2) ¿Cuál es la mejor forma de invertir en Airbnb?](#2-¿cuál-es-la-mejor-forma-de-invertir-en-airbnb)
   - [3) ¿Cómo se compara con otras alternativas de inversión?](#3-¿cómo-se-compara-con-otras-alternativas-de-inversión)
   - [4) Si presentamos nuestras conclusiones a un grupo inversor: ¿Qué propuestas le haríamos?](#4-si-presentamos-nuestras-conclusiones-a-un-grupo-inversor-¿qué-propuestas-le-haríamos)
   - [5) ¿En donde sugerimos invertir?](#5-¿en-donde-sugerimos-invertir)
   - [6) ¿En qué tipo de propiedad?](#6-¿en-qué-tipo-de-propiedad)
6. [Conclusiones](#conclusión)

## Introducción

Se eligió el dataset de Airbnb, empresa que ofrece una plataforma digital dedicada a la oferta de alojamientos, mediante la cual los anfitriones pueden publicitar y alquilar sus propiedades, y tanto anfitriones como huéspedes pueden valorarse mutuamente, como referencia para futuros usuarios.

El análisis exploratorio y descriptivo del dataset tiene como objetivo de encontrar oportunidades de inversión que puedan ser capitalizadas utilizando dicho modelo de negocio. Los datos se obtuvieron de Airbnb, para un período de 12 meses, desde el 26 de abril de 2020 hasta el 25 de abril de 2021. La información se refiere a diversos tipos de alojamiento ubicados en la Ciudad Autónoma de Buenos Aires.

##### Descripción del dataset

* Descripción de los hospedajes (tipo de propiedad, descripción del anfitrión del lugar, de la zona, de los distintos servicios y comodidades que ofrece, etc)
* Requisitos para los huéspedes (capacidad máxima de huéspedes que recibe, cantidad máxima y mínima de noches que debe reservar, precio por noche, cuyo valor valor está en pesos argentinos para el período desde abril 2020 hasta abril 2021, debiendo considerar el valor del dólar blue para dicho período, teniendo un valor promedio en la tabla listing, y la evolución del valor diario en la tabla calendar).
* Ubicación de los hospedajes (para lo cual se ofrece muchos datos, pero solo tres son los más relevantes: neighbourhood o barrio donde está ubicado -en la Ciudad de Buenos Aires-, y la latitud y longitud)
* Datos del anfitrión (nombre, cantidad de propiedades que tiene registradas en Airbnb, descripción propia, etc)
* Datos de las reseñas (reviews) y las calificaciones que dejan los huéspedes (el contenido de las mismas, la cantidad total, el promedio mensual de reseñas, distintas calificaciones con un sistema de puntos, etc).

## EDA y ETL

Se empleó PowerBI y PowerQuery como herramientas principales para trabajar con el dataset, realizar la limpieza y validación de los datos, y diseñar el dashboard. La tabla listings inicialmente constaba de 106 campos, de los cuales la mayoría fueron eliminados para conservar únicamente aquellos que resultan pertinentes para abordar las interrogantes clave del proyecto.

Se consideraron de vital importancia aquellos campos que proporcionan información sobre la ubicación de cada alojamiento, como el barrio o neighbourhood, así como la latitud y longitud para asociar los barrios con la ciudad de Buenos Aires. Además, se incluyeron campos como la capacidad máxima de personas que puede alojar (accommodates), el precio por noche (calculado como el promedio anual del precio del alojamiento, considerando también la tarifa por limpieza para determinar el precio total), el tipo de propiedad, y las reseñas por mes.

Aunque inicialmente se seleccionaron más campos, muchos fueron descartados debido a la presencia de errores o valores nulos en cantidades significativas que dificultaban la realización de análisis representativos. Otros campos fueron eliminados porque no añadían un valor sustancial o su contribución era similar a la de otros campos. Tras completar el proceso de limpieza, la cantidad de listing_id (alojamientos) se redujo de 23729 a 19906.

## Descripción del Análisis Exploratorio de los Datos:

Para explorar y describir las variables junto con sus relaciones utilizando herramientas de visualización de datos y estadísticas, se empleó PowerBI para crear un [dashboard](#dashboard-airbnb). En esta fase, se seleccionaron cuatro filtros principales: por barrio, tipo de propiedad, disponibilidad (ya sea ocupado o disponible), y fecha. Posteriormente, se incluyeron seis tarjetas informativas para presentar de manera resumida la cantidad total de hospedajes, la suma total de los precios por noche, la capacidad nocturna para albergar personas, así como tres tarjetas relacionadas con las reseñas, incluyendo el total de reseñas, el número de reseñas por mes, y un rating promedio que se calcula en base a todas las puntuaciones recibidas en los diversos aspectos relacionados con los comentarios (este rating puede servir como un indicador de la calidad de los hospedajes en un barrio específico, así como la cantidad de visitantes, dado que la mayoría deja reseñas).

#### Dashboard Airbnb
![](images/dashboard_completo_airbnb.png)

Además, se incorporaron gráficos de columnas agrupadas y líneas para examinar la evolución temporal de la demanda (según la ocupación y disponibilidad) y el precio promedio por noche. Se incluyó un mapa que visualiza la suma total del precio pagado por noche en todos los alojamientos por barrio en la ciudad de Buenos Aires, lo que permite identificar los barrios con mayor potencial de ganancias. También se agregó un gráfico de barras apiladas que muestra la distribución de distintos tipos de propiedades.

Finalmente, se añadió otro gráfico de barras apiladas que presenta, por barrio, el recuento total de alojamientos ocupados y disponibles durante un año, lo que facilita la evaluación de qué barrios reciben más visitantes anualmente.

## Preguntas

> 1) ¿Qué podemos describir con los datasets acerca del negocio de airbnb?
> 2) ¿Cuál es la mejor forma de invertir en AirBnb?
> 3) ¿Cómo se compara con otras alternativas de inversión?
> 4) Si presentamos nuestras conclusiones a un grupo inversor: ¿Qué propuestas le haríamos?
> 5) ¿En donde sugerimos invertir?
> 6) ¿En qué tipo de propiedad?

### 1) ¿Qué podemos describir con los datasets acerca del negocio de airbnb?

Podemos describir que Airbnb tiene una gran base de datos y que maneja grandes volumenes de registros en los archivos y que estos se pueden manejar con las herramientas de análisis de datos.
Con el dataset podemos describir la parte del mercado del negocio de rentas en un periodo del 12 meses desde abril del 2020 hasta abril del 2021.

El conocer, descubrir, analizar y recomendar mejor el negocio de las rentas de hospedajes en la ciudad de Buenos Aires nos ayudará a saber que decisiones de inversión para el conocimiento de los inversionistas se podrá tomar.

Así mismo, se conoce que el negocio de Airbnb tienen multiples variables que permiten conocer al negocio, a los anfitriones, la calificación de los huespedes, las políticas y restricciones de los hospedajes y la cantidad de noches ocupadas y disponibles de cada hospedaje disponible en esta plataforma. Variables de los datasets que nos dan una visión más amplia del mercado que ofrece y de la demanda que tiene en cierta temporada del año.

### 2) ¿Cuál es la mejor forma de invertir en AirBnb?

En general la mejor forma de invertir en Airbnb es conociendo el mercado a traves de los siguientes insights:

> 1. La demanda por barrio.
> 2. La demanda por tipo de hospedaje.
> 3. La rentabilidad que dejan el tipo de hospedaje.
> 4. La rentabilidad que deja el lugar geográfico ha hospedar.
> 5. La calificación que obtienen los distintos tipos de hospedaje o de barrio.

### 3) ¿Cómo se compara con otras alternativas de inversión?

El mercado inmobiliario dentro de la plataforma Airbnb a diferencia de otras alternativas, es uno de lo que ofrece mayores rentabilidades, ya que al tener contacto directo la aplicación con los huespedes hacen que el servicio sea en tiempo real y con gran variedad de opciones, esto sin importar la estación del año, precios, tipo de propiedad, etc. Lo que agrada a la demanda y esta aumente considerablemente.

### 4) Si presentamos nuestras conclusiones a un grupo inversor: ¿Qué propuestas le haríamos?

Al poder evaluar los insights se puede considerar como la mejor opción la inversión en:

1. Palermo: Mejor rendimiento y mayor cantidad de días ocupados lo que se traduce a una mayor demanda.
2. Recoleta: Es el 2do mejor lugar para invertir en departamentos para alquilar.
3. Retiro: 3er mejor lugar donde la demanda es alta y a comparación de otros lugares tiene diferentes servicios públicos.

Para determinar el mejor lugar de inversión y el tipo de propiedad nos hemos basado en la rentabilidad que deja estas variables. Para ello se creó un KPI llamado *índice de confiabilidad* que nos predispone de información relevante.

*Indice de confiabilidad = Rentabilidad / (Tasa de ocupación * 1,000,000)*

Siendo la "Tasa de ocupación" el recuento de noches no disponibles del total de hospedajes en el año y
"Rentabilidad" es la cantidad de ingresos que recibió el total de hospedajes ocupados en el mismo periodo de tiempo.

### 5) ¿En donde sugerimos invertir?

Al poder calcular el indice de confiabilidad el mejor barrio a invertir es **PALERMO**, esto se denota por nuestros graficos e indicadores:

- **Grafico de Barras:**

![alt text](images/Palermo_ind_confianza.png)

- **Grafico de barras en el año:** Nos indica como ha ido evolucionando en el barrio de Palermo, donde se ve un incremento notorio en la tasa de ocupación y en la rentabilidad, pero es necesario considerar que el recuento comienza en abril del año del 2020 momento en el cuál se encontraban las políticas de COVID que restringían el turismo razón por la cual hubo una baja considerable de la renta de alojamiento.


![alt text](images/Palermo_año.png)

Y es por las razones antes mencionadas que Palermo es el mejor lugar para invertir y de hacerlo de manera inmediata se aprovecharía el posicionamiento en el mercado por el crecimiento de la demanda en los siguientes meses.

### 6) ¿En qué tipo de propiedad?

En cuanto al tipo de propiedad elegimos para invertir la propiedad de **apartamento** por las razones siguientes:

El indice de confianza nos denota que los apartamentos son 7 veces más confiables que los condominios que están en segundo lugar, en donde la gente va a hospedarse.

![alt text](images/image.png)

En terminos de rentabilidad, se puede decir que los apartamentos en Palermo tienen una rentabilidad de alrededor 20.7 millones de dolares incluso frente a 4.9 millones de dolares que dejan los condominios.

## Conclusión

El análisis detallado del dataset de Airbnb revela una profunda comprensión del mercado de alquiler de hospedajes en la Ciudad Autónoma de Buenos Aires durante un período crucial de 12 meses. Mediante técnicas de Análisis Exploratorio de Datos (EDA) y Extracción, Transformación y Carga (ETL), se ha logrado identificar oportunidades de inversión prometedoras, destacando el barrio de Palermo como el principal candidato para obtener rendimientos significativos. La combinación de datos sobre la demanda, la rentabilidad y la satisfacción del cliente ofrece una visión completa del mercado, permitiendo a los inversores tomar decisiones informadas y estratégicas para maximizar sus retornos.

La preferencia por invertir en apartamentos en Palermo se fundamenta en la rentabilidad demostrada y la confiabilidad de este tipo de propiedad, que supera significativamente a otras opciones. Esta conclusión sólida respaldada por datos precisos brinda una guía clara para los inversores que buscan capitalizar el crecimiento y la demanda en el mercado de alquiler de hospedajes de Buenos Aires. En resumen, el análisis exhaustivo del dataset de Airbnb proporciona una hoja de ruta para la inversión exitosa en el sector, destacando la importancia de comprender las tendencias del mercado y aprovechar las oportunidades emergentes para obtener rendimientos óptimos.#   P r o y e c t o - i n t e g r a d o r - M 5 - A i r b n b  
 