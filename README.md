[![Blue-Yellow-Futuristic-Virtual-Technology-Blog-Banner.png](https://i.postimg.cc/tChDwmxC/Blue-Yellow-Futuristic-Virtual-Technology-Blog-Banner.png)](https://postimg.cc/QHdpWmmR)

# Farmaceutica Biogenesys

## Introducción
El propósito de este proyecto es aportar mediante un análisis de datos exploratorio y concluyente, bases sólidas para la toma de decisiones informadas por parte de alta gerencia para los procesos de expansión e inversión que actualmente está adelantando la compañía. 

## Objetivos Organizacionales Alcanzados
- Consolidación de datos estructurados para la toma de decisiones informadas.
- Conocimiento del mercado latinoamericano, en miras de continuar diversificando no solo los productos de la farmacéutica si no su impacto social en las comunidades. 
- Implementación de planes de expansión sólidos en miras de consolidar la compañía en el mercado latinoamericano.

## Desarrollo del Proyecto

### Phyton
Para efectos de optimización de procesos se empleó Python con el uso de las bibliotecas Numpy y Panda, en las cuales se realizaron transformaciones de datos en el Dataset, entre las cuales se incluyen:

*Lectura del archivo .CSV:* lectura del archivo brindado por el equipo de ingeniería de datos para iniciar con el proceso de analitica. 

*Visualización previa de los datos del dataset:* para confirmar el tipo de datos que presentaba así como las columnas que contenía.

*Comprobación de la data:* se comprueba que el archivo tenga los datos y las columnas suministradas por el equipo de ingeniería de datos.

*Selección de los países donde posiblemente la farmacéutica se expandirá:* aplicación de filtro al Dataset para solo trabajar con los datos requeridos.

*Verificación de filtros aplicados y comprobación de valores nulos:* se comprobó que al aplicar el filtro de países, el volumen de datos no disminuyó de manera considerable. 

*Confirmación de valores únicos:* se confirmaron cuales eran las columnas que contenían valores únicos tales como las nombradas con key, en las cuales se observó que los joins aplicados previamente alteraron el nombre de las columnas..  

*Aplicación del filtro de fecha requerido:* en miras de solo trabajar con la data requerida se aplicó este filtro para continuar con el proceso de limpieza de datos. 

*Confirmación de los valores nulos e identificación de las columnas donde se encuentran:* confirmación de estos valores y ubicación de columnas para realizar un ciclo “for” para rellenar valores faltantes. 

*Aplicación del ciclo “for”* para rellenar los valores faltantes con el promedio de los datos de la columna o con el valor “0”, dependiendo del tipo de dato: acciones que ayudaron a optimizar la calidad de los datos para poder llegar a insights y conclusiones más acertadas.
*Comprobación de valores nulos:* se vuelve a iterar sobre el dataset y se confirma que ya no presenta valores nulos. 

*Generación del nuevo archivo .CSV con los datos filtrados y limpiados:* se reinicia el notebook para poder liberar memoria y continuar con el análisis el cual al cargarse no gasto tantos recursos como el anterior. 

### Power Bi
Teniendo en cuenta el EDA que se generó en Python, en el cual en la generación de gráficos se identificaron valores atípicos, se realizó en Power Query una exploración de datos de los mismos con aplicación de filtros donde se encontraron valores atípicos de más de 10 dígitos, en relación con los datos de la columna, dichos valores se desmarcan del conjunto de datos con el fin de evitar que la generación de tarjetas y los gráficos generarán números extensos tipo notación científica que no tenían porque generarse por el tipo de dato que las columnas presentaban.

### Análisis del dashboard

Para el diseño del Dashboard, se tuvieron en cuenta los factores demográficos, etnográficos y acciones contundentes hacia el virus como la vacunación. 
Se comienza de lo general a particular, iniciando por el contexto del virus con tarjetas que dan un análisis inicial de la incidencia del mismo en los países estudiados; cuenta con filtros de año y países para ir detectando a simple vista  las diferentes variaciones que se presentan entre los mismos por año.  Se quiso demostrar inicialmente el índice de desarrollo humano, el cual define como es el desarrollo de población tanto en términos de escolaridad como acceso a los servicios de salud, como punto de partida para la reacción inicial ante una pandemia seguido por las prevalencias de diabetes y tabaquismo.

Luego se realiza un análisis general partiendo de los grupos de edad, determinantes para ver cómo afecta el virus a la población de un determinado país, las dosis acumuladas administradas muestra la cobertura y el comportamiento de los países en cuanto a la aplicación de las mismas, el personal de salud también cumple un rol importante  a la hora de poder dar respuesta inmediata a una posible pandemia y la esperanza de vida da un acercamiento a las condiciones que ofrece un país desde las perspectivas de acceso a servicios de salud de calidad y en la prevención y tratamiento de las enfermedades. Tanto las gráficas de grupos de edad como de personal de salud están realizadas bajo campos calculados en las cuales el usuario puede elegir qué gráfica desea ver desde el panel de filtros ubicado a la izquierda. 

Para concluir luego de realizar un recorrido desde el contexto del virus hasta sus generalidades, se propone que la farmacéutica se expanda inicialmente en 3 países (México, Brazil y Chile), también se sustenta la propuesta con una tabla que muestra datos clave de incidencia del virus, complementandose con gráficos de barras e histogramas que muestra la densidad poblacional y el área rural en Km² como argumentos que validan la propuesta. 

### Conclusiones y Recomendaciones

#### Conclusiones de las visualizaciones y dashboard

- El factor poblacional incide mucho en las cifras analizadas, tal es el caso de Brazil que debido a su extensión puede hasta triplicar la población de otros países, por lo cual muestra cifras altas, en cuanto a la tasa de mortalidad se hace la acotación de que Perú es el que presenta las cifras más altas siendo esta su población más reducida respecto a Brazil.
- Los grupos de edad no son determinantes a la hora de medir la mortalidad del virus ya que la población más vulnerable que es la de la tercera edad, no es alta respecto a otros grupos, por lo cual podrían tener más incidencia las comorbilidades y la prevalencia de enfermedades como la diabetes y consumo de tabaco.
- La alta tasa de mortalidad que presenta Perú respecto al virus, podría estar relacionada con su alta tasa de mortalidad por contaminación, debido a que estas partículas contaminadas pueden transportar el virus de forma eficiente.
- Se puede observar cómo la población urbana es preponderante respecto a la rural, concluyendo que las condiciones de hacinamiento y calidad del aire inciden en la rápida transmisión de los virus.
- Chile y México presentan altas cifras de prevalencia en tabaquismo y diabetes respectivamente, condiciones preexistentes que pueden agravar los síntomas de los virus e incidir en las tasas de mortalidad del mismo, respecto a las comorbilidades estos dos países no presentan cifras altas a comparación de Brazil y Argentina, por lo cual se puede inferir que su población en su mayoría esa sana.
- En cuanto a la dosis de vacunas administradas acumuladas, se nota un gran descenso en Colombia por lo cual se deben analizar las estrategias que está implementado el gobierno en cuanto a vacunación. A nivel general se pueden observar descensos y repuntes en las dosis administradas las cuales pueden deberse a factores logísticos, predisposición de las personas al vacunarse y el descenso de los contagios.

### Ubicaciones óptimas para la expansión de laboratorios farmacéuticos

Ubicaciones óptimas para la expansión de laboratorios farmacéuticos
Se eligieron países los cuales por su ubicación estratégica de norte a sur, cubren en términos logísticos la demanda de latinoamérica en el caso de Brasil y Chile como centroamérica  con México. Así mismo teniendo en cuenta el área rural por Km² predominante en Brazil y México en comparación a Chile, se propone priorizar la investigación en Chile y la producción de vacunas en Brazil y México, esta estrategia permitirá que la investigación cobre más importancia para optimizar el proceso de elaboración de vacunas, cabe aclarar que Chile también producirá vacunas para cubrir la demanda local y la de los países de Argentina, Bolivia y Paraguay. 

Se prevé que si se realiza una investigación constante se pueden detectar posibles virus altamente contagiosos e implementar de forma óptima una respuesta acertada ante posibles pandemias. 





