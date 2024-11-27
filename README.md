# Predicción de Rotación de Personal en Empresas Manufactureras de Tala, Jalisco 📊

En este repositorio se pretende desarrollar un modelo predictivo para la rotación de personal para empresas manufacturereras.

# Abstract 📝

En México la industria manufacturera presenta un alto porcentaje de rotación de personal, esto tiene un fuerte impacto económico en las empresas y por ende en la economía del país, buscando atender esta problemática e identificando el hecho de que no existe literatura acerca de la predicción de rotación de personal en la industria manufacturera de Jalisco, esta investigación tiene como objetivo el desarrollo y evaluación de algoritmos predictivos supervisados aplicados a la rotación de personal. 

# [Análisis exploratorio de datos (EDA) 🔍](results/EDA)

Se ralizó un análisis exploratorio de datos con el objetivo de limpiar el set de datos inicial y detectar variables y relaciones valiosas.

## Resultados 📝

Al iniciar el análisis exploratorio de datos, la base de datos tenía 16 variables, 502 entradas y 948 valores nulos, luego del proceso de limpieza de datos se concluyó con 14 variables, 495 registros y 0 valores núlos.

Se eliminaron las variables salario diario, ya que existe salario mensual y ambas aportan la misma información, y motivo de renuncia, que por su cantidad de valores faltantes y tratarse de texto abierto, su análisis va más allá del alcance de este estudio.

Finalmente, la visualización de datos permitió determinar que los empleados auxiliares de almacén son los que tienen una mayor rotación de personal y el personal que rola turno suele trabajar menos de 100 días antes de abandonar la empresa y que no existe una diferencia significativa entre el abandono de trabajo y el género.


# [Visualizaciones interactivas con Altair 📈](results/visuales_altair)

Este análisis se centró en crear visualizaciones para responder preguntas clave relacionadas con la dinámica laboral y salarial, proporcionando información valiosa para la toma de decisiones estratégicas en el negocio.

## Resultados 📝

### 1.-Salario por género
Se observó que los hombres tienen un salario promedio ligeramente más alto que las mujeres, aunque la diferencia es mínima.

| GENERO    |   SALARIO MENSUAL |
|:----------|------------------:|
| FEMENINO  |            7409.3 |
| MASCULINO |            8116.1 |

### 2.-Renuncias por género
Las mujeres presentan tasas de renuncia más altas, destacando que las renuncias voluntarias son las más comunes. Esto podría estar relacionado con los bajos salarios que las impulsan a buscar mejores oportunidades.

| GENERO    | Tipo de renuncia   |   Número de Renuncias |
|:----------|:-------------------|----------------------:|
| FEMENINO  | ABANDONO           |                    62 |
| FEMENINO  | ACTIVO             |                    59 |
| FEMENINO  | BAJA               |                    25 |
| FEMENINO  | VOLUNTARIA         |                   117 |
| MASCULINO | ABANDONO           |                    53 |
| MASCULINO | ACTIVO             |                    43 |
| MASCULINO | BAJA               |                    25 |
| MASCULINO | VOLUNTARIA         |                   110 |

### 3.-Salarios por departamento
El puesto de operador de prensa tiene uno de los salarios más altos, alcanzando hasta 18,000 pesos mensuales. Esto podría deberse a la experiencia o al tiempo de antigüedad en la empresa.

| PUESTO           |   SALARIO MENSUAL |
|:-----------------|------------------:|
| AUXILIAR ALMACEN |           8541.43 |
| INSP CALIDAD     |           7785.58 |
| MECANICO         |          12101.1  |
| MONTACARGUISTA   |          10107.4  |
| OP PRENSA        |           7912.08 |
| OP PRODUCCION    |           7157.84 |

### 4.-Duración en los puestos por departamento
Los departamentos con el mínimo valor de tiempo de permanencia más bajo son ALMACEN, PRENSA y PRODUCCION, todos con un mínimo de 1. Esto indica que en esos departamentos se ha registrado el menor tiempo de permanencia de una persona, es decir, al menos una persona dejó el departamento después de estar solo 1 unidad de tiempo (probablemente en días o meses).

| AREA          |   Min |    Q1 |   Mediana |     Q3 |   Max |
|:--------------|------:|------:|----------:|-------:|------:|
| ALMACEN       |     1 | 20.75 |      41.5 | 205    |   818 |
| CALIDAD       |     3 | 14.25 |      29.5 |  87    |   855 |
| MANTENIMIENTO |    17 | 28.5  |      62   | 142.25 |   514 |
| PRENSA        |     1 | 19    |      22   |  29    |   533 |
| PRODUCCION    |     1 | 20    |      44   | 155    |  1053 |


### 5.-Edad y bajas laborales
Las bajas son más frecuentes entre los 30 y 35 años. A partir de esta edad, la probabilidad de renuncia disminuye considerablemente.

| RANGO DE EDAD   |   Número de Bajas |
|:----------------|------------------:|
| 0-19            |                 4 |
| 20-29           |               127 |
| 30-39           |               291 |
| 40-49           |                44 |
| 50-59           |                26 |
| 60-69           |                 2 |
| 70-79           |                 0 |
| 80-89           |                 0 |
| 90-100          |                 0 |

### 6.-Salarios por municipio
Tlajomulco registra los salarios más altos, posiblemente debido a la presencia de empresas de alto nivel en sectores como el farmacéutico, electrónico y manufacturero.

| MUNICIPIO              |   SALARIO MENSUAL |
|:-----------------------|------------------:|
| TLAJOMULCO             |          16300    |
| CD GUZMAN              |          11200    |
| ZAMORA                 |          10065    |
| ZAPOPAN                |           8862.5  |
| SAN JUAN DE LOS ARCOS  |           8400    |
| AHUISCULCO             |           8100    |
| HUAXTLA                |           7700    |
| TALA                   |           7650.08 |
| BUENA VISTA            |           7500    |
| LA VENTA DEL ASTILLERO |           7500    |
| EL ARENAL              |           6750    |

Estas visualizaciones proporcionan una base sólida para entender los patrones salariales, las renuncias y las dinámicas laborales dentro de la organización, facilitando el diseño de estrategias más efectivas.



# [Análisis de texto ✍️](results/analisis_sentimientos)

El análisis de texto se compone de 3 secciones; N-grams para detectar patrones, análisis de sentimientos para detectar carga positiva o negativa en los comentarios y una _word cloud_ para visualizar las palabras más comunes.

## Resultados 📝

En N-grams se detectó que los empleados en su mayoría abandonan su trabajo al encontrar una mejor oferta laboral, o por problemas familiares o son despedidas por su bajo desempeño laboral.

| Token 1      | Token 2       | Frecuencia | Bigram               |
|--------------|---------------|------------|----------------------|
| mejor        | oferta        | 32         | mejor oferta         |
| problemas    | familiares    | 19         | problemas familiares |
| bajo         | desempeño     | 13         | bajo desempeño       |
| temas        | personales    | 9          | temas personales     |
| problema     | familiar      | 7          | problema familiar    |

Del análisis de sentimientos se detectó que la mayoría de párrafos tenían una conotación negativa aunque se cuestiona el resultado pudiera ser discutido ya que los motivos son más bien postulados que no se prestan a un análisis más profundo.

| Paragraph                                                  | Polarity | Subjectivity |
|------------------------------------------------------------|----------|--------------|
| PROBLEMA PERSONAL                                          | 0.000    | 0.30         |
| CONFLICTO FAMILIAR CON UNA COMPAÑERA                       | 0.375    | 0.50         |
| PROBLEMA FAMILIAR                                          | 0.375    | 0.50         |
| COMENTA QUE DONDE TOMA EL TRANSPORTE DE COOL P...          | 0.350    | 0.65         |
| PARA TRABAJAR EN LA MISMA EMPRESA A LA QUE ENTR...         | 0.350    | 0.65         |
| PROBLEMA PERSONAL                                          | 0.000    | 0.30         |

Finalmente, abajo se deja el wordcloud para su visualización:

<img src="results/analisis_sentimientos/analisis_sentimientos_wordcloud.png" alt="image" width="75%">


# Estructura de repositorio 🗂️
    
    ├── data                                            <- Base de datos original.  
    |    |── README.md                                  <- Descripción general del contenido del directorio.
    |    └── rotacion_personal.xlsx                     <- Base de datos.  
    |      
    ├── doc                                             <- Archivos de texto.
    |    └──  README.md                                 <- Problema, objetivo y justificación del proyecto.
    |
    ├── results                                         <- Resultados de los análisis realizados.
    |    |── EDA                                        <- Directorio análisis EDA.
    |    |   |──  README.md                             <- Resultados escritos del análisis EDA.
    |    |   └──  rotacion_personal_clean.csv           <- Base de datos limpia resultante de análisis EDA.
    |    |
    |    |── analisis_sentimientos                      <- Directorio análisis de texto.
    |    |   |──  anal_sent_biagram_frec.png            <- Análisis de sentimientos Biagram.
    |    |   |──  analisis_sent.png                     <- Análisis de sentimientos polaridad.
    |    |   |──  analisis_sentimientos_Biagram.png     <- Análisis de sentimientos biagrama relaciones.
    |    |   |──  analisis_sentimientos_wordcloud.png   <- Análisis de sentimientos wordcloud.
    |    |   └──  README.md                             <- Resultados escritos del análisis de texto.
    |    |
    |    |── visual_altair                              <- Directorio visualizaciones interactivas.
    |    |   └──  README.md                             <- Resultados escritos de visualizaciones interactivas.
    |    |
    |    └──  README.md                                 <- Descripción general del contenido del directorio.
    |  
    ├── src                                             <- Archivos de código.    
    |    |── EDA.ipynb                                  <- Archivo de código con análisis EDA.
    |    |── EDA_Analisis_sentimientos.ipynb            <- Archivo de código con análisis EDA de texto.
    |    |── analisis_sentimientos.ipynb                <- Archivo de código con análisis de texto.
    |    |── visual_altair.ipynb                        <- Archivo de código con análisis EDA implementando graficos de Altair Gallery
    |    └── README.md                                  <- Descripción general del contenido del directorio.
    |
    ├── CITATION.md                                     <- Cómo citar el proyecto.  
    |  
    ├── CONTRIBUTING.md                                 <- Pasos para contribuir al proyecto.  
    |   
    ├── LICENSE                                         <- MIT License.  
    |  
    └── README.md                                       <- Readme file principal con la descripción del proyecto.  
   
