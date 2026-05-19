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
