# Bulk-RNA-seq
Preparación de los datos:Se cargan y normalizan los datos de expresión génica utilizando TMM (Trimmed Mean of M-values) para ajustarlos antes de realizar el análisis de expresión diferencial.
Construcción de la matriz de diseño: Se crea una matriz de diseño para representar las condiciones experimentales, lo que ayudará a ajustar un modelo lineal de expresión génica.
Definición de contrastes experimentales: Se definen contrastes entre condiciones experimentales, como conditionUnknown_0h vs conditionBG_4h, para analizar las diferencias de expresión génica entre ellas.
Ajuste del modelo lineal: Se ajusta un modelo lineal a los datos utilizando la función lmFit(), aplicando los contrastes experimentales con contrasts.fit().
Aplicación de corrección Bayesiana: Se utiliza la función eBayes() para corregir los estadísticos del modelo y mejorar las estimaciones de los genes diferencialmente expresados.
Extracción de genes diferencialmente expresados (DEGs): Se identifican los genes con diferencias significativas en su expresión, y los resultados se guardan en archivos CSV.
Visualización de resultados (histogramas y gráficos de volcán): Se visualizan los resultados de la expresión génica con histogramas de valores p y gráficos de volcán para resaltar los genes sobreexpresados y subexpresados.
Generación de diagramas de caja: Se crean diagramas de caja (boxplots) para visualizar la expresión de los genes más significativos en función de las condiciones experimentales.
Creación de la columna condition: Se añade una columna condition que combina las columnas Treatment y Time para facilitar la identificación de las condiciones experimentales en el análisis.
Análisis de enriquecimiento funcional: Se mapean los identificadores de genes a símbolos y se realizan análisis de enriquecimiento utilizando las bases de datos KEGG y MSigDB para identificar rutas y procesos biológicos asociados con los genes diferencialmente expresados.
Este flujo resume el procesamiento, análisis y visualización de datos de expresión génica y enriquecimiento funcional en condiciones experimentales.
