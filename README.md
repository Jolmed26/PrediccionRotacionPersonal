# Predicción de Rotación de Personal en Empresas Manufactureras de Tala, Jalisco 📊

En este repositorio se pretende desarrollar un modelo predictivo para la rotación de personal para empresas manufacturereras.

# Abstract 📝

En México la industria manufacturera presenta un alto porcentaje de rotación de personal, esto tiene un fuerte impacto económico en las empresas y por ende en la economía del país, buscando atender esta problemática e identificando el hecho de que no existe literatura acerca de la predicción de rotación de personal en la industria manufacturera de Jalisco, esta investigación tiene como objetivo el desarrollo y evaluación de algoritmos predictivos supervisados aplicados a la rotación de personal. 

# Análisis exploratorio de datos (EDA) 🔍

Al iniciar el análisis exploratorio de datos, la base de datos tenía 16 variables, 502 entradas y 948 valores nulos, luego del proceso de limpieza de datos se concluyó con 14 variables, 495 registros y 0 valores núlos.

Se eliminaron las variables salario diario, ya que existe salario mensual y ambas aportan la misma información, y motivo de renuncia, que por su cantidad de valores faltantes y tratarse de texto abierto, su análisis va más allá del alcance de este estudio.

Finalmente, la visualización de datos permitió determinar que los empleados auxiliares de almacén son los que tienen una mayor rotación de personal y el personal que rola turno suele trabajar menos de 100 días antes de abandonar la empresa y que no existe una diferencia significativa entre el abandono de trabajo y el género.


# Estructura de repositorio 🗂️
    
    ├── data                            <- Base de datos original.  
    |    |── README.md                  <- Descripción general del contenido del directorio.
    |    └── rotacion_personal.xlsx     <- Base de datos.  
    |      
    ├── doc                             <- Archivos de texto.
    |    └──  README.md                 <- Problema, objetivo y justificación del proyecto.
    |
    ├── results                         <- Base de datos limpia y analizada.  
    |    └──  README.md                 <- Resultados escritos del análisis EDA.
    |  
    ├── src                             <- archivos de código.    
    |    |── EDA.ipynb                  <- Archivo de código con análisis EDA.
    |    └── README.md                  <- Descripción general del contenido del directorio.
    |  
    ├── CITATION.md                     <- Cómo citar el proyecto.  
    |  
    ├── CONTRIBUTING.md                 <- Pasos para contribuir al proyecto.  
    |   
    ├── LICENSE                         <- MIT License.  
    |  
    ├── README.md                       <- Readme file principal con la descripción del proyecto.  
   