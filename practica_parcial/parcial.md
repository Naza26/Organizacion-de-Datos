
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



