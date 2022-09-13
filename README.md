# Organizacion-de-Datos

**Herramientas a utilizar:**

  - Python3:
      1. Tensorflow
      2. Keras
      3. Numpy
      4. Pandas
      5. Pytorch
      6. Yolo
      7. TPOT
      8. Scikit-learn
      
  - Weka
  - Maquinas Jupiter
  - Kaggle
  
**¿Qué es un Data Scientist?**
  
  Es aquel capaz de:
  
    - Obtener, interpretar, procesar y filtrar datos
    - Llegar a conclusiones a partir de los datos obtenidos
    - Construir solcuiones para los problemas que se quiere solucionar
    
**Data Scientist != Data Engineer**

- Considerable solapamiento entre las habilidades y responsabilidades
- Hay una importante diferencia en el enfoque
- El ingeniero de datos se enfoca en la creacion de la infraestructura y arquitectura para la generacion, soporte y extraccion de los datos (Big Data)
- El cientifico de datos se enfoca en la interpretacion y analisis de los datos mediante el analisis estadistico y matematico


![Screen Shot 2022-08-25 at 16 51 57](https://user-images.githubusercontent.com/50343570/186755512-4bf7befc-0158-451a-96e7-93f47b9727f5.png)

**Habilidades Tecnicas**

- Data Mining
- Visualizacion de Datos
- Matematica y Estadistica
- Machine Learning
- Plataformas: Linux, AWS, Google Cloud

**¿Que es machine learning (def: 2019)?**

El aprendizaje automatico es la ciencia y arte de programar computadoras para que aprendan a partir de datos

Aprendizaje Automatico:

- Filtros de Spam (Enfoque Tradicional vs Enfoque ML)

**¿Para que se utiliza ML?**

- Salud
- Gaming
- Energia
- Turismo
- Seguridad

**Metodologia**

- Entender el problema
- Recolectar los datos
- Procesar los datos
- Explorar los datos
- Analizar los datos
- Comunicar los resultados


 ## Visualizacion de Datos

**¿Por qué es necesario graficar?**

- Las tecnicas de visualizacion de datos son muy importantes tanto para nuestro trabajo como para comunicarlo
- La cantidad de tipos de graficos disponibles es enorme y es importante entenderlos y saber por qué es util cada uno
- Entender de forma eficiente los datos
- Comunicar de forma concisa y clara
- Encontrar patrones/relaciones


**Por qué es necesario graficar?**

- El analisis descriptivo es uno de las partes principales de cualquier analisis relacionado con un proyecto de ciencia de datos o de una investigacion especifica
- La agregacion de datos, el resumen, y la visualizacion son algunos de los pilares que respaldan esta area
- La visualizacion de datos es una herramienta poderosa y ampliamente adoptada debido a su efectividad para extraer la informacion correcta, comprender e interpretar los resultados de manera clara y facil
- Tratar con conjuntos de datos multidimensionales con mas de una variable o atributo comienza a causar problemas, ya que estamos restringidos a comunicar en dos dimensiones (a lo sumo 3)


**Datasaurus**

Todos estos graficos tienen la misma media y desvio estandar

**Visualizacion para ML**

- Analisis inicial de los datos
  - Para examinar si los datos satisfacen los supuestos requeridos para el metodo
  - Tienen complicaciones inesperadas como valores atipicos o no linealidad
- Evaluar el ajuste del modelo
  - Predicho vs Observado
  - Analisis de Residuos

**Plots**

1. De distribucion continua:

    Eje X = Soporte Continuo (NO discreto).
  
    Eje Y = Cantidad o Similar.
  
  - Histograma:
  
    Eje Y = Que empiece en cero (0)
  
    Numero apropiado de bins. Por ejemplo bin size = 5.0
  
    Limite de bins interpretables (enteros por ejemplo)
  
  - Density Plot:

    Eje Y = Densidad (Poco interpretable, ya no sabemos las cantidades)
  
    Suavizar los bordes para lograr la densidad, o sabe que no tiene sentido < 0
  
  - Box Plot:

    Un diagrama de caja o Box plot muestra visualmente la distribución de los datos numéricos y la asimetría mediante la visualización de los cuartiles
    (o percentiles) y los promedios de los datos.
    
3. De distribucion discreta
  - Bar Plot
  - Stacked Bar Plot
  - Treemap
4. De relacion
  - Scatter Plot
  - Regression Plot
  - HeatMap
6. Series de tiempo
  - Lineplot
  - Violin Plots
8. Otros

**Pandas CheatSheet**

[Pandas_Cheat_Sheet.pdf](https://github.com/Naza26/Organizacion-de-Datos/files/9438408/Pandas_Cheat_Sheet.pdf)

<img width="1195" alt="Screen Shot 2022-08-27 at 14 29 49" src="https://user-images.githubusercontent.com/50343570/187041421-0007a2ec-b69a-44b2-999f-5905c7586aec.png">


<img width="1188" alt="Screen Shot 2022-08-27 at 14 30 05" src="https://user-images.githubusercontent.com/50343570/187041428-6126bdc5-f477-49c3-839a-0bbcb8d4a218.png">


## Tipos de Variables

1. Categoricas o Cualitativas

Las distintas modalidades que adoptan estas variables sólo se distinguen por ser diferentes, no se puede establecer un ordenamiento entre ellas. Son ejemplos de estas variables: color de cabello, tipo de auto, sexo.

2. Cuasicuantitativas u Ordinales

En estas variables, si bien se puede ordenar las modalidades que adopta, no se puede establecer una distancia entre ellas. Por ejemplo: calificación de examen (A, B, C, D y E), estadío de una enfermedad (I, II, III o IV).

3. Cuantitativas Discretas

Estas variables toman valores numéricos siendo que entre dos valores consecutivos de las mismas no existen valores intermedios. Pueden tomar un conjunto a lo sumo numerable de valores, vinculándose generalmente al proceso de contar. Son ejemplos de estas variables: cantidad de hijos, cantidad de materias aprobadas, dinero en una billetera.

4. Cuantitativas Continuas

Estas variables también toman valores numéricos, pero entre dos valores de la variable existen infinitos valores intermedios, asociándose generalmente al proceso de medir. Son ejemplos de estas variables: peso, edad, duración de un llamado


## Correlacion de Pearson

Los diagramas de dispersión son útiles para ver si dos variables están
correlacionadas

Para 2 variables podemos medir su correlación lineal con el coeficiente de correlación r (Pearson). Este coeficiente, es
una función que mide cuán relacionada estan 2 variables de forma lineal.

- Si da 0, NO existe correlacion
- Si da 1 estan relacionadas linealmente de forma PERFECTA (todos los puntos estan en una linea)
- Si da -1 existe una correlacion NEGATIVA perfecta
