# Modelo_para_prediccion_desercion_clientes
Los clientes de Beta Bank se están yendo, necesitamos predecir si un cliente dejará el banco pronto. Se tienen los datos sobre el comportamiento pasado de los clientes y la terminación de contratos con el banco.

## **Conclusión general**

En conclusión durante el preprocesamiento de los datos se observó la presencia de algunos valores ausnetes en la columna de `Tenure` el cual contiene información sobre el período durante el cual ha madurado el depósito a plazo fijo de un cliente (años) cuya ausencia lo que puede significar que no posee ningún depósito de este típo, por lo cual el espacio se dejó en blanco y para no perder las caracteríasticas simplemenete sustituiremos el valor por 0.

Además no existe un valor demasiado claro que nos permita determinar si un cliente se irá o no, vemos que las variaciones son bastente sutiles, es por eso que se recurre al Machine Learning

Así mismo, se intentó utilizar un m,odelo de regresión logística en el cual no obtuvimos bueno resultados, por lo que se decide cambiar a un modelo de bosque aleatorio de decisión

Luego, podemos conlcuir en este caso con el modelo de arbol aleatorio de decisión al separar los conjuntos de datos, es posible obtener resultados bastente óptimos, que al apliacar conjuntos externos de datos, nos permiten predecir con muy buena precisión y exactitud los resultados que queremos, en este caso obtuvimos los siguientes valores:

* F1 = 60.8 %
* recall = 55.56 %
* precision = 67.14 %
* Auc-Roc = 84.33 %
* Excatitud = 85.1 %

Lo que quiere decir que se tiene un modelo lo suficientemente bueno como para tener una exactitud del 85,1% con buenos niveles de sensibilidad y presición el cual no toma desiciones aleatorias, siendo ápto para predecir si un cliente se va a ir o no del banco y poder tomar las medidas necesarias para que este se mantenga
