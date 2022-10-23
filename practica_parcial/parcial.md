
## Introduccion a la ciencia de datos


### Variables

- Variables Independientes (entradas)
- Variables dependientes (salidas, categorías)


Variables Independientes:
  - Cualitativas
    - Texto
      - Nominales (categorías, ejemplo: países)
      - Ordinales (poco, mucho, muchísimo)
    - Númericas
      - Nominales
      - Ordinales

  - Cuantitativa
    - Discreta
    - Continua


### Variables y tipos de problemas

1. Si la variable dependiente es cualitativa, el tipo de problema es de clasificación
2. Si la variable dependiente es cuantitativa, el problema es de regresión
3. Si NO hay variable dependientes, el problema es de agrupamiento

- Outliers (valor atípico)


### Correlacion de variables

Dos variables están correlacionadas cuando varían de igual forma sistemáticamente.

1. Positiva
2. Negativa
3. Sin Correlacion


-> Correlación NO IMPLICA Causalidad

- Que dos variables tengan alto índice de correlación no significa que una cause la otra
- Las relaciones de causalidad son mucho más difíciles de encontrar y demostrar
- Las correlaciones pueden suceder por otros motivos como: Una tercer variable que “empuja” a ambas o simplemente azar

### Varianza

Promedio de la diferencia, entre todas las observaciones, respecto de su media.

### Covarianza

En probabilidad y estadística, la covarianza es un valor que indica el grado de variación conjunta de dos variables aleatorias respecto a sus medias.
Es el dato básico para determinar si existe una dependencia entre ambas variables y además es el dato necesario para estimar otros parámetros básicos, como el coeficiente de correlación lineal o la recta de regresión.

<img width="771" alt="Screen Shot 2022-10-11 at 19 57 02" src="https://user-images.githubusercontent.com/50343570/195213314-811a94c8-b95a-4dd4-ba4a-9ecb847bff43.png">
<img width="779" alt="Screen Shot 2022-10-11 at 19 57 28" src="https://user-images.githubusercontent.com/50343570/195213361-e2bee584-4665-4587-a6cc-32b07599de86.png">
<img width="747" alt="Screen Shot 2022-10-11 at 19 57 42" src="https://user-images.githubusercontent.com/50343570/195213390-4566607b-54e6-4bcb-a82e-db987a79c911.png">

### Correlacion de pearson

Para 2 variables podemos medir su correlación lineal con el coeficiente de correlación r (Pearson). Este coeficiente, es una función que mide cuán relacionada estan 2 variables de forma lineal.

- Si da 0 NO existe correlación

- Si da 1 Están relacionadas linealmente de forma perfecta (todos los puntos están en una línea)

- Si da -1 Existe una correlación negativa perfecta.

### Correlacion de pearson, desvio estandar

Es una medida que se utiliza para cuantificar la variación o la dispersión de un conjunto
de datos numéricos. Una desviación estándar baja indica que la mayor parte de los datos de una muestra
tienden a estar agrupados cerca de su media (también denominada el valor esperado), mientras que una desviación estándar alta indica que los datos se extienden sobre un rango de valores más amplio.

<img width="395" alt="Screen Shot 2022-10-11 at 19 59 41" src="https://user-images.githubusercontent.com/50343570/195213593-cff17898-d60b-46c2-9577-01089dc9797f.png">


### Regresion

Buscamos predecir un valor en un rango continuo, para ciertos valores de entrada. Ejemplos:

- Temperatura
- Valor de una propiedad

<img width="703" alt="Screen Shot 2022-10-11 at 20 01 22" src="https://user-images.githubusercontent.com/50343570/195213790-ca685459-1148-48be-abe7-5808a37ec569.png">

<img width="479" alt="Screen Shot 2022-10-11 at 20 02 34" src="https://user-images.githubusercontent.com/50343570/195213902-8095bd9c-0b87-4e40-a6cb-f7ca62797a78.png">

### Problemas con la ecuacion normal

Si se duplica el número de características, el tiempo se multiplica por aproximadamente 2^3 = 8.
Existen otros mecanismos que buscan de forma iterativa, por aproximación y son computacionalmente menos costosos como el descenso por gradiente.

<img width="713" alt="Screen Shot 2022-10-11 at 20 05 15" src="https://user-images.githubusercontent.com/50343570/195214170-8f24f454-d6e9-48a9-ab85-21722e2624f5.png">

### Metodos de clasificacion

Cuando resolvemos un problema de clasificación, buscamos, para ciertos datos de entrada, un categoría c de un conjunto C de
categorías posibles. Estas categorías no solo son finitas, sino que además son conocidas de antemano.

### Regresion logistica

En la regresión logística lo que quiero es categorizar, clasificar. Es decir que dado una serie de puntos quiero encontrar una función (no es una recta en este caso) que separe los puntos en dos, en dos
conjuntos.
Y una vez que la encontré puedo determinar para cualquier valor X futuro,
el conjunto al cual pertenecerá. Está asociado a problemas de
probabilidad.

### Metodos de Clusterizacion

**Clustering**

En este tipo de problemas se trata de agrupar los datos. Agruparlos de tal forma que queden definidos N conjuntos distinguibles, aunque no necesariamente se sepa que signifiquen esos conjuntos. El agrupamiento siempre será por características similares.

**K-Means**

1. El usuario decide la cantidad de grupos
2. K-Means elige al azar K centroides
3. Decide qué grupos están más cerca de cada centroide. Esos puntos forman un grupo
4. K-Means recalcula los centroides al centro de cada grupo
5. K-Means vuelve a reasignar los puntos usando los nuevos centroides. Calcula nuevos
grupos
6. K-means repite punto 4 y 5 hasta que los puntos no cambian de grupo.

<img width="723" alt="Screen Shot 2022-10-11 at 20 09 24" src="https://user-images.githubusercontent.com/50343570/195214638-1e2eb00b-0a1b-40d3-b551-ef65882073e6.png">

<img width="752" alt="Screen Shot 2022-10-11 at 20 09 43" src="https://user-images.githubusercontent.com/50343570/195214666-f9f1304b-cd5e-479b-b935-5568aa933ff0.png">


<img width="723" alt="Screen Shot 2022-10-11 at 20 10 19" src="https://user-images.githubusercontent.com/50343570/195214709-36ebc5cd-27e1-4d2b-aae7-6dcd3f06cd03.png">

### ¿Cuantos conjuntos elegir?

A veces es obvio, si estamos trabajando con el conjunto MNIST claramente son 10 conjuntos los que tengo. Si estoy trabajando con el conjunto IRIS serán 3.

### Regla del codo (Elbow Method)

<img width="678" alt="Screen Shot 2022-10-11 at 20 16 25" src="https://user-images.githubusercontent.com/50343570/195215371-0e548241-6343-4917-a67b-9fbb36d141d5.png">

### Metodo Silhouette

1. Elegimos un rango, ejemplo 1 a 10, y para cada valor:
  - Para cada valor de K graficamos la silhouette
    - El mejor valor posible es silhouette = 1
    - El peor valor posible es silhouette = -1


Primeramente tendremos que calcular el coeficiente de Silhouette.

### Coeficiente de Silhouette

Cada punto en el conjunto de datos tiene un coeficiente de Silhouette. Para calcular este coeficiente necesitamos calcular a(i) y b(i).


<img width="722" alt="Screen Shot 2022-10-11 at 20 18 20" src="https://user-images.githubusercontent.com/50343570/195215590-40c9edc4-c9f2-4052-a8ac-211ec3208018.png">

<img width="745" alt="Screen Shot 2022-10-11 at 20 18 40" src="https://user-images.githubusercontent.com/50343570/195215631-0082ebde-7376-449d-9613-64aa1e03f770.png">

<img width="694" alt="Screen Shot 2022-10-11 at 20 18 59" src="https://user-images.githubusercontent.com/50343570/195215674-546ba828-3b14-41e7-9369-d57a3b6ca9f5.png">

<img width="700" alt="Screen Shot 2022-10-11 at 20 19 26" src="https://user-images.githubusercontent.com/50343570/195215736-deb69210-c379-4bf2-bcde-fbc5a3c41162.png">

<img width="799" alt="Screen Shot 2022-10-11 at 20 19 48" src="https://user-images.githubusercontent.com/50343570/195215770-08f683db-aa1b-4b8e-baeb-e3c35bba1360.png">

### Estadistica de Hopkins

La estadística de Hopkins (Lawson y Jurs 1990) se utiliza para evaluar la tendencia de agrupación de un conjunto de datos midiendo la probabilidad de que un conjunto de datos dado sea generado por una distribución de datos uniforme. En otras palabras, prueba la aleatoriedad espacial de los datos.

<img width="739" alt="Screen Shot 2022-10-11 at 20 20 51" src="https://user-images.githubusercontent.com/50343570/195215865-38631591-c37d-4e9d-84db-5432277a50f3.png">

<img width="701" alt="Screen Shot 2022-10-11 at 20 21 19" src="https://user-images.githubusercontent.com/50343570/195215912-413500e3-8f31-4b9d-8eff-da9beb55bf86.png">

La idea es comparar una muestra cualquiera con una muestra uniforme (creada de forma aleatoria) y ver cómo se distribuyen los ejemplos (los puntos) en dicho espacio.

Sea D un conjunto de datos reales:


<img width="775" alt="Screen Shot 2022-10-11 at 20 22 24" src="https://user-images.githubusercontent.com/50343570/195216017-07ee2f7f-c943-4391-acda-bc53115fcba5.png">

**Estadistica de Hopkins: Hipotesis**

Hipótesis que maneja Hopkins:

  - Hipótesis nula: el conjunto de datos D se distribuye uniformemente (es decir, no hay clusters significativos)
  - Hipótesis alternativa: el conjunto de datos D no está uniformemente distribuido (es decir, contiene clusters significativos)

Podemos realizar la prueba de la estadística de Hopkins de forma iterativa, utilizando 0,5 como umbral para rechazar la hipótesis alternativa.
  - Es decir, si H < 0,5, es poco probable que D tenga conglomerados estadísticamente significativos.
  - O si el valor de la estadística de Hopkins es cercano a 1, entonces podemos rechazar la hipótesis nula y concluir que el conjunto de datos D es   significativamente un dato agrupable.

### Entrenamiento 

<img width="708" alt="Screen Shot 2022-10-11 at 20 24 19" src="https://user-images.githubusercontent.com/50343570/195216209-ad39ede2-2805-4ea0-ab9a-880948f56636.png">

<img width="711" alt="Screen Shot 2022-10-11 at 20 24 40" src="https://user-images.githubusercontent.com/50343570/195216244-a18e93cb-2340-4e64-bf10-fe5ed9cf7462.png">

<img width="786" alt="Screen Shot 2022-10-11 at 20 24 56" src="https://user-images.githubusercontent.com/50343570/195216260-6627a8a1-0071-47f2-a3f1-8da0ebe8b251.png">

<img width="715" alt="Screen Shot 2022-10-11 at 20 25 11" src="https://user-images.githubusercontent.com/50343570/195216281-7a348186-af54-49e9-92fb-c0529d58d3dd.png">

<img width="735" alt="Screen Shot 2022-10-11 at 20 25 30" src="https://user-images.githubusercontent.com/50343570/195216309-629270e9-f221-4ac4-a777-017c7a525d57.png">

### Metricas

<img width="734" alt="Screen Shot 2022-10-11 at 20 27 44" src="https://user-images.githubusercontent.com/50343570/195216533-433e94c6-7fde-4be6-88b8-6caf9a0aa427.png">

<img width="755" alt="Screen Shot 2022-10-11 at 20 28 10" src="https://user-images.githubusercontent.com/50343570/195216601-97a262b7-8d8f-4726-8e1c-a2de77fef3cd.png">

<img width="732" alt="Screen Shot 2022-10-11 at 20 28 21" src="https://user-images.githubusercontent.com/50343570/195216628-752e3cf5-df22-4969-bd99-ec8e5eaf6bec.png">


<img width="734" alt="Screen Shot 2022-10-11 at 20 29 00" src="https://user-images.githubusercontent.com/50343570/195216713-966e76a0-d659-4fd4-975b-05105bb8d40b.png">


## Ingenieria de Features

**Preprocesamiento y transformacion de datos**

Algunas tareas de estas etapas son:
  - **Integración de datos**: Integración de múltiples bases de datos, archivos, etc.
  - **Limpieza de datos**: Completar valores faltantes, eliminación de ruido, identificar o eliminar valores atípicos y corregir incoherencias
  - **Reducción de datos**: Reducción de dimensionalidad, Reducción de Numerosidad
  - **Transformación de datos**: Normalizaciones, generación de jerarquías conceptuales, etc. (Feature Engineering)


Limpieza de datos

- No solo NANs
- MCAR (Missing completly at random)
- MNAR (Missing not at random)
- MAR (Missing at random)

Tipos de datos faltantes:

MCAR: 

La falta de valores no tiene nada que ver con la persona o el objeto estudiado. No existen relaciones con la variable misma donde se encuentran los datos faltantes, o con las restantes variables en el dataset que expliquen porque faltan.
Por ejemplo, una muestra de sangre puede ser dañada en un laboratorio. 

MNAR:

La razón por la cual faltan los datos depende precisamente de los mismos datos que hemos recolectado (está relacionado con la razón por la que falta). Por ejemplo, una persona que no atiende a un test de drogas porque la noche anterior las consumió.

MAR:

La causa de los datos faltantes no depende de estos mismos datos faltantes, pero puede estar relacionada con otras variables del dataset. Por ejemplo: encuestas mal diseñadas, que me pregunten si tengo hijos, que yo repsonda que no y que luego me pregunten que deportes practican mis hijos, ahi seguro lo dejo en blanco y el valor resulta faltante.

Estrategias para trabajar con datos faltantes

**Eliminar registros o variables**

Si la eliminación de un subconjunto disminuye significativamente la utilidad de los datos, la eliminación del caso puede no ser efectiva (No se recomienda en situaciones que no sean MCAR).


**Imputar datos**

Utilizar métodos de relleno de faltantes.


**Imputacion de Datos**

**1. Sustitución de casos**

Se reemplaza con valores no observados. Debería ser realizado por un experto en esos datos.

**2. Sustitución por Media o Mediana**

Se reemplaza utilizando la medida calculada de los valores presentes.

Algunas desventajas:

- La varianza estimada de la nueva variable no es válida porque está atenuada por los valores repetidos
- Se distorsiona la distribución
- Las correlaciones que se observen estarán deprimidas debido a la repetición de un solo valor constante

**3. Imputacion Cold Deck***

Selecciona valores o usa relaciones obtenidas de fuentes distintas de la base de datos actual.

<img width="695" alt="Screen Shot 2022-10-22 at 14 02 43" src="https://user-images.githubusercontent.com/50343570/197353021-63f5496c-fbe0-4426-abdd-0f7977ea7439.png">

**3. Imputacion Hot Deck***

Se reemplazan los faltantes con valores obtenidos de registros que son los más similares. (Hay que definir que es similar, K vecinos más cercanos puede servir)

<img width="694" alt="Screen Shot 2022-10-22 at 14 03 39" src="https://user-images.githubusercontent.com/50343570/197353068-3b986800-16eb-429d-96dd-86290b4ecf36.png">


**4. Imputacion por regresion**

El dato faltante es reemplazado con el valor predicho por un modelo de regresión.


<img width="732" alt="Screen Shot 2022-10-22 at 14 04 30" src="https://user-images.githubusercontent.com/50343570/197353102-ef1ff735-a2b9-421b-83b6-739e3609d063.png">

**5. MICE - Multivariate Imputation by Chained Equations** 

Trabaja bajo el supuesto de que el origen de los faltantes es Missing At Random (MAR). Es un proceso de imputación de datos faltantes iterativo, en el cual, en cada iteración cada valor faltante de cada variable se predice en función de las variables restantes. Esta iteración se repite hasta que se encuentre convergencia en los valores. Por lo general 10 iteraciones es suficiente. (En cada iteración genera un dataset)

**Feature Engineering**

Esta etapa incluye cualquier proceso de modificación de la forma de los datos (es común que los datos sufran algún tipo de transformación).

El objetivo principal de esta etapa es mejorar el rendimiento de los modelos creados mediante la transformación de los datos que utilizan.

Algunas técnicas son:

  - Normalización

  - Discretización

  - Lograr normalidad

  - Imaginación ( Generación de nuevas variables )

**Normalizacion**

Se aplica sobre valores numéricos. Consiste en escalar los features de manera que puedan ser mapeados a un rango más pequeño.

Por ejemplo: 0 a 1 o -1 a 1.

Es principalmente utilizada cuando:
  - Las unidades de medidas dificultan la comparación de features.
  - Se quiere evitar que atributos con mayores magnitudes tengan pesos muy diferentes al resto

**Normalizacion - Min Max**

Funciona al ver cuánto más grande es el valor actual del valor mínimo del feature y escala esta diferencia por el rango.

Los valores de normalización min-max van de 0 a 1.

**Normalizacion - Zscore**

Los valores para un atributo se normalizan en base a su media y desvío estándar.
Es útil cuando el verdadero mínimo y máximo del atributo no son conocidos, o cuando hay valores atípicos que dominan la normalización min-max.

**Normalizacion - Decimal Scaling**

Asegura que cada valor normalizado se encuentra entre - 1 y 1.
Donde d representa el número de dígitos en los valores de la variable con el valor absoluto más grande.


<img width="789" alt="Screen Shot 2022-10-22 at 14 13 44" src="https://user-images.githubusercontent.com/50343570/197353512-5765aeb6-6d90-4a9c-89ef-c718cb377edb.png">

**Transforamcione spara lograr normalidad**

Podemos reducir este sesgo a partir de transformaciones, por ejemplo:
  - Raíz cuadrada
  - Logaritmos
  - Inversa de la raíz cuadrada
  - Transformaciones de Box-Cox

**Discretaizacion**

Es una técnica que permite dividir el rango de una variable continua en
intervalos.

Se reducen los valores de una variable contínua a un número reducido de
etiquetas.

**Discretaizacion - Binning**

Se divide a la variable en un número específico de bins

Los criterios de agrupamiento pueden ser por ejemplo:
  - Igual-Frecuencia: La misma cantidad de observaciones en un bin
  - Igual-Ancho: Definimos rangos o intervalos de clases para cada bin
  - Cuantiles: Separar en intervalos utilizando Mediana, Cuantiles,Percentiles.

A su vez para cada uno de los agrupamientos podemos hacer:
  - Reemplazo por media o mediana
  - Reemplazo por una etiqueta o valor entero

<img width="792" alt="Screen Shot 2022-10-22 at 14 16 26" src="https://user-images.githubusercontent.com/50343570/197353630-5cd3bafd-a6a2-455c-b356-1f09dafd4ed6.png">

**Variables Dummies - One Hot Encoding**

Algunos métodos analíticos requieren que las variables predictoras sean numéricas
Cuando tenemos categóricos, podemos recodificar la variable categórica en una o más variables Dummies.


<img width="762" alt="Screen Shot 2022-10-22 at 14 17 32" src="https://user-images.githubusercontent.com/50343570/197353664-1cac3049-9ce9-4f04-9af8-22bc0ca16835.png">

### Analisis de Valores Atipicos

“Un outlier es una observación que se desvía tanto de las otras observaciones como para despertar sospechas que fue generado por un mecanismo diferente”

- Es un concepto subjetivo al problema.
- Son observaciones distantes del resto de los datos
- Pueden deberse a un error de medición, aleatoriedad, que esa instancia pertenezca a una familia distinta del resto, etc.

Ejemplo 1: Una persona de 120 años de edad
Ejemplo 2: Una persona de 4 años que mide 1.80mts


<img width="276" alt="Screen Shot 2022-10-23 at 11 59 13" src="https://user-images.githubusercontent.com/50343570/197399360-d804bb9e-482a-43d7-8dd5-6fff1d1e6315.png">

¿Es necesario eliminarlos?

- Deben ser cuidadosamente inspeccionados
- Pueden estar alertando anomalías, en algunas situaciones nuestra tarea de interés será encontrarlos.

Tipos de Outliers


<img width="710" alt="Screen Shot 2022-10-23 at 12 00 30" src="https://user-images.githubusercontent.com/50343570/197399402-b16c8827-3f24-4920-a772-ff0d40d53fe2.png">


En grandes volúmenes de datos la detección de outliers resulta más eficiente estudiando todas las variables.

Los outliers, en casos multivariados, pueden provocar dos tipos de efectos:

El efecto de enmascaramiento se produce cuando un grupo de outliers esconden a otro/s. Es decir, los outliers enmascarados se harán visibles cuando se elimine/n el o los outliers que los esconden.


El efecto de inundación ocurre cuando una observación sólo es outlier en presencia de otra/s observación/es. Si se quitara/n la/s última/s, la primera
dejaría de ser outlier.


<img width="776" alt="Screen Shot 2022-10-23 at 12 02 39" src="https://user-images.githubusercontent.com/50343570/197399508-2553c9ec-f184-492a-9238-3c1669e1c820.png">

<img width="766" alt="Screen Shot 2022-10-23 at 12 03 02" src="https://user-images.githubusercontent.com/50343570/197399530-63fa6ba9-3d27-4c1e-be3c-6e7c172f3c8d.png">

**UNIVARIADOS**

**Zscore**

Z-Score es una métrica que indica cuántas desviaciones estándar tiene una observación de la media muestral, asumiendo una distribución gaussiana.
Cuando calculamos Z-Score para cada muestra debemos fijar un umbral:

- Un valor como “regla de oro” es Z > 3

**Zscore modificado**

La media de la muestra y la desviación estándar de la muestra, pueden verse afectados por los valores extremos presentes en los datos.

Regla de oro:

- Valores mayores a 3.5 son considerados outliers


**Analisis de Boxplot**

Los Box-Plots permiten visualizar valores extremos univariados.
Las estadísticas de una distribución univariada se resumen en términos de cinco cantidades:

- Mínimo/máximo (bigotes)
- Primer y tercer cuantil (caja)
- Mediana (línea media de la caja)
- IQR = Q3 - Q1

Generalmente la regla de decisión:
+/- 1.5*IQR Outliers moderados
+/- 3 *IQR Outliers severos


Problema

Una forma de tratar valores atípicos es eliminar los valores más altos y más bajos de una variable.

Esto puede funcionar bastante bien, pero no tiene en cuenta las combinaciones de variables.


**MULTIVARIADOS**

**Distancia de Mahalanobis**


<img width="743" alt="Screen Shot 2022-10-23 at 12 08 44" src="https://user-images.githubusercontent.com/50343570/197399848-4e7d11c3-f686-4d1a-ad35-22c8409b2b0b.png">

**LOF - Local Outlier Factor**


<img width="782" alt="Screen Shot 2022-10-23 at 12 12 32" src="https://user-images.githubusercontent.com/50343570/197400087-599a39ec-daca-45f7-b1c1-d92be62f2cab.png">

**Isolation Forest**


<img width="779" alt="Screen Shot 2022-10-23 at 12 15 12" src="https://user-images.githubusercontent.com/50343570/197400204-a7e7ef1a-8460-4d96-ae98-12b4f4a632a7.png">

Tomar una muestra de los datos y construir un árbol de
aislamiento:

1. Seleccionar aleatoriamente n características .
2. Dividir los puntos de datos seleccionando aleatoriamente un valor entre el mínimo y el máximo de las características seleccionadas.

La partición de observaciones se repite recursivamente hasta que todas las observaciones estén aisladas.

Isolation Forest identifica anomalías como las observaciones con longitudes de ruta promedio cortas en los árboles de aislamiento.

## Arboles

**ID3 (Iterative Dichotomiser 3)**

Genera un árbol de decisión a partir de un conjunto de ejemplos.

Representación de un Árbol de decisión
La salida del algoritmo ID3 se representa como un grafo en forma de árbol, cuyos componentes son:

<img width="435" alt="Screen Shot 2022-10-23 at 12 24 35" src="https://user-images.githubusercontent.com/50343570/197400761-eb0a6f2e-6f3e-4ae3-808b-a53403ae4871.png">


<img width="938" alt="Screen Shot 2022-10-23 at 12 25 29" src="https://user-images.githubusercontent.com/50343570/197400809-5d45bde3-607f-4ceb-97ad-ca0fe99eaf3d.png">


**ID3 - Entropia (de la información)**

La medida del desorden o la medida de la pureza. Básicamente, es la medida de la impureza o aleatoriedad en los datos.

Importante

- Para una muestra homogénea la entropía es igual a 0

- La máxima entropía viene dada por Log2(n), n son los posibles valores de salida. 
- Si n =2 (TRUE o FALSE) entonces, la máxima entropía es 1. O sea es la máxima incertidumbre

**ID3 - Ganancia de información:**

La ganancia de información se aplica para cuantificar qué característica, de un conjunto de datos dados, proporciona la máxima información sobre la clasificación.
Si tuviésemos que elegir una sola característica, para clasificar. ¿Cuál sería?

**ID3 - Algoritmo básico:**

1. Calcular la entropía para todas las clases.
2. Calcular la entropía para cada valor posible de cada atributo.
3. Seleccionar el mejor atributo basado en la reducción de la entropía. Usando el cálculo de
Ganancia de la Información
4. Iterar, para cada sub-nodo. Excluyendo el nodo raíz, que ya fue usado.

<img width="959" alt="Screen Shot 2022-10-23 at 12 30 20" src="https://user-images.githubusercontent.com/50343570/197401072-59eb8664-0c6d-45d6-b68d-4d09a78c7c00.png">


<img width="947" alt="Screen Shot 2022-10-23 at 12 30 33" src="https://user-images.githubusercontent.com/50343570/197401083-c27c8b37-0e6e-43d0-a3fe-62736a03515a.png">

<img width="951" alt="Screen Shot 2022-10-23 at 12 30 58" src="https://user-images.githubusercontent.com/50343570/197401101-7f55d66e-0237-4fef-9752-9fdf0a7661de.png">

<img width="955" alt="Screen Shot 2022-10-23 at 12 31 08" src="https://user-images.githubusercontent.com/50343570/197401106-f7865083-f272-49f2-9f93-eebe80f87f02.png">


<img width="952" alt="Screen Shot 2022-10-23 at 12 31 24" src="https://user-images.githubusercontent.com/50343570/197401120-70b1e91e-f740-4226-a143-8aabce850233.png">


<img width="933" alt="Screen Shot 2022-10-23 at 12 32 17" src="https://user-images.githubusercontent.com/50343570/197401170-96cd3342-1731-4254-9a5a-8b7330feef73.png">


<img width="951" alt="Screen Shot 2022-10-23 at 12 32 39" src="https://user-images.githubusercontent.com/50343570/197401191-bf67d80a-d555-460a-9acc-f9343b764514.png">


<img width="956" alt="Screen Shot 2022-10-23 at 12 32 49" src="https://user-images.githubusercontent.com/50343570/197401195-181a8a03-0f53-40c0-9a24-e3ba426c8cda.png">

<img width="937" alt="Screen Shot 2022-10-23 at 12 32 59" src="https://user-images.githubusercontent.com/50343570/197401204-788ffa99-4fb1-472a-b23b-789c2206e2a9.png">


<img width="910" alt="Screen Shot 2022-10-23 at 12 33 12" src="https://user-images.githubusercontent.com/50343570/197401220-10c36fe9-769b-4477-b64c-835d83f6865f.png">

<img width="909" alt="Screen Shot 2022-10-23 at 12 33 33" src="https://user-images.githubusercontent.com/50343570/197401234-f14a4d57-ea00-43f4-b6c6-c3d269e1733e.png">


<img width="947" alt="Screen Shot 2022-10-23 at 12 33 42" src="https://user-images.githubusercontent.com/50343570/197401240-2d909602-4491-41e1-8fb0-33da3ed52878.png">


<img width="959" alt="Screen Shot 2022-10-23 at 12 34 31" src="https://user-images.githubusercontent.com/50343570/197401290-40c434a2-faf2-4d24-8007-858991c94582.png">


<img width="949" alt="Screen Shot 2022-10-23 at 12 34 42" src="https://user-images.githubusercontent.com/50343570/197401295-db879a84-b4d2-4f73-8c54-58a7a23c14ac.png">


<img width="957" alt="Screen Shot 2022-10-23 at 12 34 54" src="https://user-images.githubusercontent.com/50343570/197401301-cbe53b92-1552-4867-bb7c-2717561c9211.png">

<img width="884" alt="Screen Shot 2022-10-23 at 12 35 02" src="https://user-images.githubusercontent.com/50343570/197401313-82a8c095-1692-4848-8efa-ab222c4422b6.png">


- Un nodo de decisión está asociado a uno de los atributos y tiene 2 o más ramas que salen de él, cada una de ellas representando los posibles valores que puede tomar el atributo asociado.

- Un nodo-respuesta está asociado a la clasificación que se quiere proporcionar,y nos devuelve la decisión del árbol con respecto al ejemplo de entrada.

**Impureza de Gini**

La impureza de Gini es una medida de cuán a menudo un elemento elegido aleatoriamente del conjunto sería etiquetado incorrectamente si fue etiquetado de manera aleatoria de acuerdo a la distribución de las etiquetas en el subconjunto

Algunas implementaciones de árboles de decisión utilizan la impureza de Gini en lugar de la ganancia de información, ya que es más fácil de calcular (computacionalmente menos costosa) Ejemplo: Scikit-learn

<img width="418" alt="Screen Shot 2022-10-23 at 12 37 55" src="https://user-images.githubusercontent.com/50343570/197401429-04a15778-d7b5-4d0d-9d11-1324d3201bd5.png">


<img width="972" alt="Screen Shot 2022-10-23 at 12 38 34" src="https://user-images.githubusercontent.com/50343570/197401458-3cda0631-af58-486a-8553-8250f73043c8.png">


<img width="960" alt="Screen Shot 2022-10-23 at 12 38 49" src="https://user-images.githubusercontent.com/50343570/197401475-466712e4-f0fc-4772-8b05-17622d310c86.png">

<img width="962" alt="Screen Shot 2022-10-23 at 12 39 01" src="https://user-images.githubusercontent.com/50343570/197401483-019cf627-bce5-4dca-8e15-674946f6fb4c.png">


<img width="960" alt="Screen Shot 2022-10-23 at 12 39 21" src="https://user-images.githubusercontent.com/50343570/197401494-4e26e18f-e93f-4fb4-b1e8-90a456b2a002.png">


Para saber cual clasifica mejor, tenemos que medir la impureza de cada nodo y de cada árbol.

Hay varias formas de medir esto, una muy popular es llamada: Gini


<img width="962" alt="Screen Shot 2022-10-23 at 12 39 56" src="https://user-images.githubusercontent.com/50343570/197401519-804a0af1-3dda-46f9-a87f-595f9a66b82b.png">


<img width="927" alt="Screen Shot 2022-10-23 at 12 40 09" src="https://user-images.githubusercontent.com/50343570/197401526-bb320a62-3c81-4512-9bf9-96124c1c23d9.png">

<img width="936" alt="Screen Shot 2022-10-23 at 12 40 20" src="https://user-images.githubusercontent.com/50343570/197401545-a00cbcfb-4658-42ee-9856-1ce569590cf8.png">


<img width="953" alt="Screen Shot 2022-10-23 at 12 41 09" src="https://user-images.githubusercontent.com/50343570/197401592-698c9c9c-c14c-4148-906a-be9941845460.png">


<img width="944" alt="Screen Shot 2022-10-23 at 12 41 23" src="https://user-images.githubusercontent.com/50343570/197401599-a29390a9-6a06-47f2-8b25-c972d0c776b4.png">


<img width="950" alt="Screen Shot 2022-10-23 at 12 41 41" src="https://user-images.githubusercontent.com/50343570/197401616-aabf8808-aa83-4e37-badf-21dc846513af.png">

**C4.5**

Se hicieron mejoras a ID3
- Campos numéricos, rangos continuous
- Datos faltantes
- Poda

**C4.5: Datos faltantes**


Datos faltantes:

Manejo de los datos de formación con valores de atributos faltantes - C4.5 permite valores de los atributos para ser marcado como “?” para faltantes. Los valores faltantes de los atributos simplemente no se usan en los cálculos de la ganancia y la entropía.

**C4.5: Campos numéricos, o rangos continuous**

Campos numéricos, o rangos continuous:

Si un atributo A, tiene un rango continuo de valores. El algoritmo puede, dinámicamente crear
un campo Booleano tal que si A < C Ac = TRUE, sino Ac = FALSE.

¿Cómo encontrar ese umbral C?

Vamos a cortar el rango de forma que C nos quede con la mayor ganancia de información.

Ordenamos A de menor a mayor, por ejemplo.
Identificamos los valores adyacentes (de la clase que es nuestra salida)
Detectamos cuando hay un cambio de valor de salida, entonces en esos límites seguramente están nuestros Ci candidatos. 
Creamos varios Ci, que dividen en dos el rango. Para cada uno de estos rangos calculamos la ganancia de información. Nos quedamos con el que nos
da el mejor resultado. (Se puede también quedarse con los N mejor.)


**C4.5: Poda**

El método de poda del árbol consiste en:
 generar el árbol tal y como hemos visto


A continuación, analizar recursivamente, y desde las hojas, qué preguntas (nodos interiores) se pueden eliminar sin que se incremente el error de clasificación con el conjunto de test.
(Si hay ruido el árbol tendrá un error, es decir cantidad de casos mal clasificados)
Error= Casos bien clasificados / Casos Totales

El método de poda del árbol consiste en:
Se elimina un nodo interior cuyos sucesores son todos nodos hoja.
Se vuelve a calcular el error que se comete con este nuevo árbol sobre el conjunto de test.
Si este error es menor que el error anterior, entonces se elimina el nodo y todos sus sucesores(hojas)
Se repite.


**Random Forest**

“Muchos estimadores mediocres, promediados pueden ser muy buenos”


Es una técnica, o meta-algoritmo que dice lo siguiente:
Dado un conjunto de entrenamiento D, de tamaño n, la técnica de bagging generará m nuevos conjuntos de entrenamiento D1,... Di,..., Dm cada uno de tamaño n' tomando muestras aleatorias de D. 
Y  en general n'<n. Siendo n' aproximadamente un 2⁄3 de n.


Attribute bagging (o random subspace): 

Luego para cada una de las m tablas, escogemos sólo algunos atributos (COLUMNAS) de forma aleatoria también.

¿Con cuantas nos quedamos?  =>Con RAÍZ CUADRADA del número de atributos.

Cómo acá hay 8 atributos, tomamos Round(√8) = 3 
(Esto es recomendable sobre todo cuando hay muchas columnas)


Ahora tenemos m tablas reducidas en atributos y para cada una de ellas entrenamos un árbol
Para cada árbol calculamos su matriz de confusión:


<img width="549" alt="Screen Shot 2022-10-23 at 15 49 22" src="https://user-images.githubusercontent.com/50343570/197410159-47d2e933-8a4f-4577-bc86-c20e1bea651d.png">


<img width="876" alt="Screen Shot 2022-10-23 at 15 50 30" src="https://user-images.githubusercontent.com/50343570/197410210-d7ac5239-a9f3-4a1a-8db2-f703af9451c3.png">


¿Cómo clasificar una vez finalizado el proceso?

Luego para clasificar un nuevo ejemplo hacemos lo siguiente:

Ejecutamos el caso que queremos probar por cada uno de los K arboles
Si la mayoría de los casos devolvió que la categoría final es CATEGORIA-A,
entonces nos quedamos con ese valor de salida.

## Reduccion de la dimensionalidad

**ISOMAP**

¿Qué pasa cuando tenemos una variedad, usando la definición matemática, sobre la cual están distribuidos los datos?

Una variedad es una porción del espacio, de dimensión n que se parece a ℝn, en un espació de dimensión mayor.

Hipótesis de variedades

Esta hipótesis sostiene que la mayoría de los conjuntos de datos de alta dimensión del mundo real quedan cerca de una variedad con muchas menos dimensiones.
Este supuesto se observa a menudo de forma empírica. 


<img width="963" alt="Screen Shot 2022-10-23 at 16 04 54" src="https://user-images.githubusercontent.com/50343570/197410773-90e0b58b-941e-4a4e-86e8-b2b8d157392e.png">


<img width="951" alt="Screen Shot 2022-10-23 at 16 46 13" src="https://user-images.githubusercontent.com/50343570/197414643-80f60bb0-c020-4283-a6b5-0e6b5c3d44c0.png">


<img width="912" alt="Screen Shot 2022-10-23 at 16 47 05" src="https://user-images.githubusercontent.com/50343570/197414683-ded6548c-23da-4db0-8d2b-75dd336c7492.png">

<img width="946" alt="Screen Shot 2022-10-23 at 16 47 39" src="https://user-images.githubusercontent.com/50343570/197414703-404ad677-fe6b-4f1d-9ace-3adcc0419563.png">


<img width="907" alt="Screen Shot 2022-10-23 at 16 48 01" src="https://user-images.githubusercontent.com/50343570/197414741-299c4a53-abc8-4d44-8217-447a9a0bf60b.png">


**Debilidades**

Es un algoritmo lento,  a partir de 1000 observaciones comienza a notarse la lentitud.
puede crear una proyección errónea si k es demasiado grande con respecto a la estructura de la variedad o si hay ruido en los datos, de tal forma que los puntos aparecen ligeramente movidos, fuera de la variedad. Incluso un solo dato mal medido puede alterar muchas entradas en la matriz de distancia geodésica. 
Si k es demasiado pequeño, el gráfico de vecindad puede volverse demasiado escaso para aproximar las trayectorias geodésicas con precisión. 

Landmark ISOMAP

Tengo N datos especiales, siendo que N es menor que el número total de datos. Y solo tomo las distancias que involucran a estos N datos especiales. 
Los puedo elegir de forma uniformemente distribuida.
Luego se aplica Landmark-MDS (LMDS) en la matriz de distancias calculadas para encontrar una proyección euclidiana de todos los puntos en el conjunto original de datos.

**t-SNE**

Se trata de otro método que al igual que PCA, toma datos de un espacio de alta dimensión y los proyecta en un espacio de menor dimensión para que puedan ser representados.


<img width="932" alt="Screen Shot 2022-10-23 at 17 14 16" src="https://user-images.githubusercontent.com/50343570/197416000-f8d08e7d-be74-4db6-8247-919be2ff859a.png">


<img width="961" alt="Screen Shot 2022-10-23 at 17 14 53" src="https://user-images.githubusercontent.com/50343570/197416016-fa3f8b55-2be1-4687-9cb3-6d3eadb8eb46.png">


<img width="942" alt="Screen Shot 2022-10-23 at 17 15 42" src="https://user-images.githubusercontent.com/50343570/197416082-382882bd-66e3-436a-aa01-eb0e540c4e18.png">


<img width="941" alt="Screen Shot 2022-10-23 at 17 16 00" src="https://user-images.githubusercontent.com/50343570/197416108-205b3d19-ae66-4ee3-be34-33d5ed43186f.png">


<img width="964" alt="Screen Shot 2022-10-23 at 17 16 34" src="https://user-images.githubusercontent.com/50343570/197416132-2465930d-ec5e-4a9b-a114-243a08e06062.png">

cómo las curvas no son iguales, hay que normalizar la similitud:
Similitud/Suma de todas las similitudes = Similitud escalada = puntaje (score)

En realidad, t-SNE tiene un parámetro llamado “perplejidad” (perplexity) que es igual a la densidad esperada para un punto. 
La desviación estándar se define por este valor de perplejidad que corresponde al número de vecinos alrededor de cada punto. Este valor lo establece el usuario de antemano y permite estimar la desviación estándar de las distribuciones gaussianas definidas para cada punto xi. 
Cuanto mayor es la perplejidad, mayor es la variación.

t-SNE promedia los dos puntajes de similitud, en ambas direcciones para unificar el valor.


En Resumen:

Fortalezas:
  - De lo mejor para visualizar datos
  - Conserva estructuras no lineales globales y locales

Debilidades:
  - Es estocástico (es no determinista)
  - Escala mucho en tiempo con dimensiones y puntos
  - No se puede usar para nuevos puntos


**MDS: Multidimensional Sclaing y PCoA: Principal Coordinate Analysis**

Idea: 

- Preservar las distancias entre puntos 
- Ubicar los puntos en una dimensión menor tal que las distancias se parezcan lo más posible

La distancia calculada puede ser cualquiera, por ejemplo la euclidiana.

Ahora tengo que encontrar una nueva matriz M con la misma cantidad de columnas (es decir ejemplos) pero menos filas, 2 (según las dimensiones que quiera visualizar)

Para esta nueva Matriz voy a calcular las distancias. Generando una segunda matriz de distancias, que deberá ser lo más parecida a la original.

¡Queremos preservar las distancias! -> Siempre

Para encontrar los valores que minimicen la función de Stress hay varios algoritmos matemáticos, como:

- Método de descenso empinado de Kruskal  (Kruskal’s steepest descent method): un método de descenso por gradiente
- Método iterativo de mayorización de De Leeuw (De Leeuw’s iterative majorization method), también llamado SMACOF

Una cosa importante a tener en cuenta es que estos métodos son enfoques iterativos, que a veces dan resultados diferentes.

*+MDS: Descenso por gradiente**

La técnica de descenso por gradiente es una técnica genérica, utilizada en muchos algoritmos, la podemos usar en regresión lineal para ajustar la mejor recta, en PCA y por supuesto es una parte fundamental del algoritmo backpropagation utilizado para el entrenamiento de redes neurales 


Se trata de encontrar el mínimo de la función de error, utilizando para ello el gradiente como brújula. Ya que el gradiente apunta siempre en la dirección de máximo crecimiento, ir en la dirección opuesta nos acercará al mínimo.


<img width="962" alt="Screen Shot 2022-10-23 at 19 20 33" src="https://user-images.githubusercontent.com/50343570/197420895-bed48cb7-6b3c-4516-ba15-191429c46e81.png">


<img width="970" alt="Screen Shot 2022-10-23 at 19 20 44" src="https://user-images.githubusercontent.com/50343570/197420904-c1838904-4423-4bad-9d7c-7ca68eba7e0d.png">


El cálculo que se hizo para el componente A1MDS1, hay que repetirlo para todos los componentes y en N pasos iterativos ir achicando el error cada vez más, hasta llegar a cero o al menor valor posible (el mínimo de la función de error).
Cabe destacar que en general las raíces se las elimina de la ecuación para facilitar los cálculos, y lo que se intenta minimizar es el error cuadrático (es decir el error al cuadrado, o sin la raíz) ya que minimizar el error cuadrático es lo mismo que minimizar el error real.

En este ejemplo se calculó la derivada con la raíz cuadrada, para no perder la forma original de la función de error. 


<img width="944" alt="Screen Shot 2022-10-23 at 19 23 49" src="https://user-images.githubusercontent.com/50343570/197421044-c0d15455-50d2-4a68-9bdd-7206ddeea4cd.png">


<img width="952" alt="Screen Shot 2022-10-23 at 19 26 41" src="https://user-images.githubusercontent.com/50343570/197421133-3d6239eb-b3fa-41b4-87f7-26cda9a202e3.png">


<img width="952" alt="Screen Shot 2022-10-23 at 19 28 21" src="https://user-images.githubusercontent.com/50343570/197421201-dcafc93a-a5dd-4a08-99aa-59b0c170b22f.png">


Fortalezas:

  - Soporta varios tipos de distancias
  - Permite transformaciones no lineales

Debilidades:

  - Optimización iterativa con mínimos locales
  - Difícil determinar que distancia a usar es la mejor





