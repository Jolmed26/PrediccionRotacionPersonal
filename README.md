# Predicción de Rotación de Personal en Empresas Manufactureras de Tala, Jalisco 📊

En este repositorio se pretende desarrollar un modelo predictivo para la rotación de personal para empresas manufacturereras.

# Abstract 📝

En México, la industria manufacturera registra un elevado porcentaje de rotación de personal, lo que genera un fuerte impacto económico tanto en las empresas como en la economía nacional. Ante esta problemática, y considerando la ausencia de literatura específica sobre la predicción de rotación en la industria manufacturera de Jalisco, esta investigación tiene como objetivo desarrollar y evaluar algoritmos predictivos supervisados aplicados a este fenómeno.

# Análisis exploratorio de datos (EDA) 🔍

Al iniciar el análisis exploratorio, la base de datos contaba con 16 variables, 502 registros y 948 valores nulos. Tras el proceso de limpieza de datos, se redujo a 14 variables, 495 registros y 0 valores nulos.

Se eliminaron las variables salario diario, ya que su información era redundante con salario mensual, y motivo de renuncia, debido a su alto porcentaje de valores faltantes y al ser un campo de texto abierto que excede el alcance de este estudio.

Finalmente, la visualización de los datos reveló que los empleados auxiliares de almacén presentan la mayor rotación de personal. Además, se observó que los trabajadores que alternan turnos suelen permanecer menos de 100 días antes de dejar la empresa. Por otro lado, no se identificaron diferencias significativas en el abandono del trabajo entre géneros.


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
   
