# Pildora_perceptron
Hoy nos sumergimos en el apasionante mundo del deep lerning y para empezar comprenderemos las bases de las redes neuronales.

----

![frank](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSOcd1oCI-XtwJrj-CNlFWCgN48BJ6pYXENAg&s)

Pero como no empezar con Frank Rosenblatt considerado el padre del deep learnig, psicólogo estadounidense nacido en 1928 en New Rochelle ( Nueva York).

En el año 1958 propuso el desarrollo de un autómata eléctrico cuyo funcionamiento, sobre bases radicalmente diferentes a la de los modelos computacionales de entonces. El funcionamiento de la nueva máquina se inspiraría más bien en el funcionamiento del cerebro y de los sistemas neuronales biológicos antes que en el de los ordenadores construidos hasta entonces.

![neurona](https://media.telefonicatech.com/telefonicatech/uploads/2021/1/1692_Capturadepantalla2018-07-19alas18.05.40.png)

Como se puede observar en la imagen estamos ante una neurona humana ya que Rosenbatt se inspiro en las neuronas humanas para crear este modelo, si te fijas en la neurona humana la anatomia es la siguiente:

La neurona adquiere informacion en las conexiones denominadas dendritas, las denditras reciben la información, esta información es procesada en el núcleo, gracias a un impulso de salida esta información se transfiere através del axón que contiene terminales que estan conectadas a otras neuronas.

----

![perceptrón](https://media.telefonicatech.com/telefonicatech/uploads/2021/1/1692_Capturadepantalla2018-07-19alas12.45.09.png)
Simple ¿verdad?, el perceptrón que propone Rosenbatt no es tan distinto a lo que acabas de leer.

* **Entrada**: El input en el algoritmo del perceptrón se entienden como un vector compuesto por x1, x2, x3, x4 y así sucesivamente. Todas estas entradas denotan los valores del perceptrón de características y la ocurrencia total de las características.

* **Pesos**: Se observan como valores que se planifican al largo de la sesión de preparación del perceptrón. Los pesos ofrecen un valor preliminar en el inicio del aprendizaje del algoritmo. Con la ocurrencia de cada inexactitud de entrenamiento, los valores de los pesos se actualizan. Estos se representan principalmente como w1, w2, w3, w4 y así sucesivamente.
  
* **Función de activación**: Cada función de activación, o no lineal, toma un único número y realiza una determinada operación matemática fija sobre él. Hay varias funciones de activación que se pueden encontrar en la práctica, las más comunes son la Sigmoide o la ReLU o unidad lineal rectificada.

* **Suma ponderada**: Es la proliferación de cada valor de entrada o característica asociada con el valor de paso correspondiente.
  
* **Salida**: La suma ponderada se pasa a la función de activación y cualquier valor que obtengamos después del cálculo es nuestra salida predicha.

----
Como observaste se mira cierta similitud y hay algo importante que recalcar antes de entrar de lleno al algoritmo.

![IBM 704](https://media.licdn.com/dms/image/v2/D4D12AQFHeOtrbxjXTg/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1715098892825?e=1754524800&v=beta&t=wP0s8COlMjPO4x0ZbmNvUR1POj0zCVJAOWOam0Cj490)

En 1957 se implementó en un programa ( software) el funcionamiento del Perceptrón por primera vez utilizando un IBM704, fue el primer ordenador comercial (se vendieron 123 unidades) que utilizaba operaciones en coma flotante capaz de ejecutar 40.000 instrucciones por segundo (un Intel Core i7 es capaz de realizar aproximadamente más de 100.000 MIPS, millones de instrucciones por segundo). 

![maquina](https://media.telefonicatech.com/telefonicatech/uploads/2021/1/1692_Capturadepantalla2018-07-19alas17.42.08.png)

El Perceptrón estaba destinado a ser realmente una máquina en vez de un algoritmo y por eso finalmente se construyó el Mark I Perceptron, basado en las ideas del Perceptrón de Frank Rosenblatt. El Mark I Perceptron se dedicaba exclusivamente a la clasificación de imágenes. Todo el hardware estaba construido a medida y utilizaba potenciómetros para determinar los pesos de cada entrada por Perceptrón así como una cámara capaz de producir imágenes de 400 pixeles de resolución (20x20). En este enlace se puede encontrar el manual de operación original y en la siguiente foto se puede apreciar el panel de conexiones con las distintas combinaciones de entrada.

Aunque en principio la idea del Perceptrón tuvo una buena recepción muy prometedora en los ámbitos académicos, al final se probó que no podía ser entrenado para reconocer muchos otros tipos de patrones, lo que provocó un estancamiento en el avance de las redes neuronales durante algunos años. En ese entonces el perceptróntenía una sola capa y por lo tanto sólo eran capaces de aprender datos que permitan una separación lineal . Por lo tanto, las únicas pruebas que se realizaron con este Mark I fueron entrenar al Perceptrón para que fuera capaz de reconocer imágenes, en concreto diferenciar si es hombre o mujer.

La capacidad de proceso, la tasa de acierto, así como los patrones a analizar aumentaron cuando unos años más tarde aparecieron las redes neuronales multicapas, o perceptrón multicapa . Pero no tenemos que desmerecer el gran trabajo de Frank Rossenblatt ya que esta redes multicapas no son más que capas de muchos Perceptrón exactamente iguales al implementado en el Mark I Perceptron.

La meta de Rosenbatt era crear una maquina capaz de percibir, reconocer e identificar todos sus alrededores sin que tuviera el entrenamiento explícito o el control de un humano. nada lejos de nuestra realidad actual, ¿No crees?.

----

## desglosando las matemáticas del perceptrón

 El perceptrón realiza un mapeo que convierte unas determinadas entradas en una determinada salida.

 Como viste anteriormente el conjunto entradas del perceptrón se representa con un vector X [X1, X2, X3....Xn].

 El perceptrón toma estas entradas y realiza una combinación lineal de ellas. Para esto necesita un conjunto de parámetros denominados pesos W [W1, W2, W3...Wn], tras esto genera un valor intermedio denominado h que es el resultado de la multiplicación de los vectores X y los pesos W elemento por elemento.

 El valor intermedio *h* pasa por una función *f* que se denomina función de activación, generando la salida *f(h)= y*
 
![matematicas](https://blog.damavis.com/wp-content/uploads/2021/03/1-3.png)

En cuanto a la función de activación su rol principal es el de tratar de establecer si se encontro ciertas conbinaciones o un patrón en esas entradas. (si o no).

Es decir si tuvieramos una imagen de entrada y quisieramos saber si en esa imagen existe un gato o no existe un gato, para ello usamos una función escalón que nos permite obtener un valor de salida 1 o 0.

También puedes notar que vamos a estar convirtiendo nuestras entradas a un valor binario, para formalizar aun mas esto lo pondriamos de esta forma: *P(X): IR^n -> {0, 1}

En cuanto al sesgo o bias primero recordemos lo que es una línea recta: y = mx + b

*m* es la pendiente, la que nos indica como va la recta o si tiene una cierta inclinación, y para mover esa recta de ariba hacia abajo usamos el desplazamiento *b*

![full formula](https://miro.medium.com/v2/resize:fit:1400/0*Ib3_FfuOy04kOmfO)




## fuentes
[Historia de la ia](https://telefonicatech.com/blog/historia-de-la-ia-frank-rosenblatt-y-e)

[IMB 704](https://www.linkedin.com/pulse/el-ibm-704-un-hito-en-la-historia-de-computaci%C3%B3n-william-montilla-cqecf/)

[El Perceptrón a detalle](https://www.youtube.com/watch?v=DvbA-ZLxve8)
