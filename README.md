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

* **Entrada**: Las entradas en el algoritmo del perceptrón se entienden como x1, x2, x3, x4 y así sucesivamente. Todas estas entradas denotan los valores del perceptrón de características y la ocurrencia total de las características.

* **Pesos**: Se observan como valores que se planifican al largo de la sesión de preparación del perceptrón. Los pesos ofrecen un valor preliminar en el inicio del aprendizaje del algoritmo. Con la ocurrencia de cada inexactitud de entrenamiento, los valores de los pesos se actualizan. Estos se representan principalmente como w1, w2, w3, w4 y así sucesivamente.
  
* **Función de activación**: Cada función de activación, o no lineal, toma un único número y realiza una determinada operación matemática fija sobre él. Hay varias funciones de activación que se pueden encontrar en la práctica, las más comunes son la Sigmoide o la ReLU o unidad lineal rectificada.

* **Suma ponderada**: Es la proliferación de cada valor de entrada o característica asociada con el valor de paso correspondiente.
  
* **Salida**: La suma ponderada se pasa a la función de activación y cualquier valor que obtengamos después del cálculo es nuestra salida predicha.

----
Como observaste se mira cierta similitud y hay algo importante que recalcar antes de entrar de lleno al algoritmo
