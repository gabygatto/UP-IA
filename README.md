# UP-IA-TP 1
# Análisis Exploratorio de Datos (EDA) - Airbnb Buenos Aires

## Objetivo del trabajo

El objetivo del presente trabajo es realizar un análisis exploratorio de datos (EDA) utilizando un dataset de alojamientos de Airbnb correspondientes a la ciudad de Buenos Aires.

A través de tareas de limpieza, transformación y visualización de datos, se busca identificar patrones relevantes, detectar valores atípicos y analizar relaciones entre variables del dataset. Asimismo, el trabajo pretende validar distintas hipótesis relacionadas con características de los alojamientos, disponibilidad, reviews y valoraciones de los usuarios.

---

# Contexto del dataset

El dataset utilizado corresponde a publicaciones de alojamientos de Airbnb en la ciudad de Buenos Aires y fue obtenido desde Inside Airbnb, una plataforma que recopila información pública relacionada con anuncios de Airbnb alrededor del mundo.

El archivo analizado (`listings.csv`) contiene información descriptiva sobre los alojamientos, incluyendo:
- características estructurales,
- capacidad,
- disponibilidad,
- reviews,
- ratings,
- y datos del host.

El dataset original contenía una gran cantidad de columnas, incluyendo variables vacías o irrelevantes para el análisis, por lo que se realizó un proceso de reducción y limpieza antes de comenzar el EDA.

Cantidad aproximada de registros utilizados:
- 27.348 filas

Cantidad de variables analizadas:
- 23 columnas

---

# Diccionario de datos

| Variable | Descripción |
|---|---|
| id | Identificador único del alojamiento |
| last_scraped | Fecha de extracción del registro |
| host_is_superhost | Indica si el host es superhost |
| host_identity_verified | Indica si la identidad del host fue verificada |
| neighbourhood_cleansed | Barrio del alojamiento |
| property_type | Tipo de propiedad |
| room_type | Tipo de habitación/alojamiento |
| accommodates | Cantidad de huéspedes permitidos |
| bathrooms | Cantidad de baños |
| bedrooms | Cantidad de dormitorios |
| beds | Cantidad de camas |
| minimum_nights | Cantidad mínima de noches requeridas |
| availability_30 | Disponibilidad en los próximos 30 días |
| availability_60 | Disponibilidad en los próximos 60 días |
| availability_90 | Disponibilidad en los próximos 90 días |
| availability_365 | Disponibilidad en los próximos 365 días |
| number_of_reviews | Cantidad total de reviews |
| number_of_reviews_ltm | Reviews realizadas en los últimos 12 meses |
| review_scores_rating | Rating general del alojamiento |
| review_scores_cleanliness | Rating de limpieza |
| review_scores_location | Rating de ubicación |
| review_scores_value | Rating de relación precio/calidad |
| reviews_per_month | Cantidad promedio de reviews por mes |

---

# Metodología aplicada

El trabajo fue desarrollado utilizando Python en Jupyter Notebook y las librerías:
- Pandas
- NumPy
- Matplotlib
- Seaborn

Las etapas principales del análisis fueron las siguientes:

## 1. Carga y reducción del dataset
- Importación del archivo CSV
- Eliminación de columnas completamente vacías
- Selección de variables relevantes para el análisis

## 2. Limpieza y transformación de datos
- Conversión de tipos de datos
- Transformación de variables booleanas
- Tratamiento de valores nulos mediante imputación con mediana
- Verificación de consistencia del dataset

## 3. Análisis exploratorio de datos (EDA)
Se realizaron:
- estadísticas descriptivas,
- análisis de distribuciones,
- detección de valores atípicos,
- análisis de correlaciones,
- y estudio de relaciones entre variables.

## 4. Visualizaciones realizadas
Se generaron distintos gráficos para facilitar la interpretación de los datos:
- Histogramas con KDE
- Boxplots
- Scatterplots
- Hexbinplots
- Gráficos de barras
- Heatmap de correlaciones

## 5. Conclusiones
Finalmente, se analizaron las hipótesis planteadas inicialmente y se elaboraron conclusiones generales sobre el comportamiento del mercado de alojamientos de Airbnb en Buenos Aires.


---

# Hipótesis planteadas

## Hipótesis 1
Los hosts categorizados como superhosts poseen mejores valoraciones promedio que los hosts normales.

## Hipótesis 2
Existe una relación positiva entre la capacidad de huéspedes (`accommodates`) y la cantidad de camas (`beds`) disponibles en el alojamiento.

## Hipótesis 3
La mayoría de los alojamientos presentan una cantidad baja de noches mínimas requeridas para realizar una reserva.

## Hipótesis 4
Las valoraciones de los alojamientos tienden a ser altas y presentan baja dispersión.

## Hipótesis 5
Existen valores atípicos significativos en variables relacionadas con disponibilidad, cantidad de reviews y noches mínimas.

---

# Conclusiones

## Conclusión Hipótesis 1
El análisis de ratings promedio según la categoría de superhost no mostró diferencias relevantes entre ambos grupos. Tanto los superhosts como los hosts normales presentan valoraciones altas y relativamente similares dentro del dataset analizado.

## Conclusión Hipótesis 2
El scatterplot mostró una tendencia general positiva entre la capacidad de huéspedes (`accommodates`) y la cantidad de camas (`beds`). Sin embargo, la relación presenta una dispersión considerable y múltiples valores atípicos, por lo que no puede considerarse una asociación estrictamente lineal.

## Conclusión Hipótesis 3
La distribución de `minimum_nights` presentó una fuerte asimetría positiva. La mediana observada fue baja, indicando que la mayoría de los alojamientos requieren pocas noches mínimas para reservar. Sin embargo, se detectaron algunos valores extremos muy elevados, posiblemente asociados a alquileres de larga duración.

## Conclusión Hipótesis 4
Las variables relacionadas con ratings presentaron medias cercanas al valor máximo posible y desvíos estándar relativamente bajos. Esto sugiere que la mayoría de los alojamientos poseen valoraciones positivas y que las calificaciones otorgadas por los usuarios tienden a concentrarse en rangos altos, mostrando una dispersión reducida.

## Conclusión Hipótesis 5
El análisis exploratorio permitió detectar valores atípicos significativos en variables como `minimum_nights`, `number_of_reviews` y `availability_365`. Estos registros extremos se observaron tanto en las estadísticas descriptivas como en los boxplots realizados, evidenciando comportamientos poco frecuentes y una elevada dispersión en determinadas variables del dataset.

---

# Conclusión general

El análisis exploratorio realizado sobre el dataset de Airbnb correspondiente a la ciudad de Buenos Aires permitió identificar diversos patrones relevantes en la oferta de alojamientos publicada en la plataforma.

Se observó una predominancia de propiedades con valoraciones altas y una baja cantidad de noches mínimas requeridas en la mayoría de los casos. Asimismo, se detectó una importante heterogeneidad en variables relacionadas con disponibilidad y cantidad de reviews.

El análisis también permitió identificar valores atípicos significativos en distintas variables del dataset, evidenciando la existencia de comportamientos poco frecuentes dentro de la plataforma. Las visualizaciones realizadas facilitaron la comprensión tanto de las distribuciones generales como de las relaciones entre variables, destacándose particularmente la tendencia positiva entre capacidad de huéspedes y cantidad de camas, aunque con una dispersión considerable.

Finalmente, el dataset presentó una calidad adecuada para el desarrollo del EDA y las tareas de limpieza, transformación e imputación de datos permitieron construir un conjunto de datos consistente para el análisis.
