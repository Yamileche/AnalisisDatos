# Predicción de precio de autos

En este análisis se describirá el proceso para obtener una estimación del precio de un auto dado ciertas características. El conjunto de datos puede consultarse en  el siguiente link: https://www.kaggle.com/datasets/mohidabdulrehman/ultimate-car-price-prediction-dataset

A continuación se da una descripción del conjunto de datos 

* Id: un identificador único para cada listado de automóviles.
* Price: El rango de precios de los autos, con etiquetas de precios y conteos específicos.
* Company Name: El nombre de la empresa fabricante del automóvil, con porcentajes de representación de cada empresa.
* Model Name: El nombre del modelo de los autos, con porcentajes de representación de cada modelo.
* Model Year: el rango de años de fabricación del automóvil, con recuentos y porcentajes.
* Location: La ubicación de los autos, especificando las regiones donde están disponibles para su compra, junto con sus porcentajes.
* Mileage: Información sobre el kilometraje de los autos, con rangos de kilometraje, conteos y porcentajes.
* Engine Type: Descripciones de los tipos de motor, con porcentajes para cada tipo.
* Engine Capacity: La capacidad del motor varía con recuentos y porcentajes.
* Color: La distribución de colores de los coches, con porcentajes para cada color.

Este conjunto de datos, que contiene 46.000 entradas válidas, ofrece información valiosa sobre el mercado de automóviles usados, incluidos precios, representación del fabricante, disponibilidad del modelo y diversas especificaciones como año del modelo, ubicación, kilometraje, tipo de motor, capacidad del motor y preferencias de color. Puede ser un recurso valioso para analizar y comprender las tendencias en la industria de automóviles usados.

## Análisis y exploración
Para comenzar, veamos la cantidad de autos en venta de las 10 compañías con más autos a la venta, podemos observar que Suzuki, Toyota, Honda y Daihatsu tienen más autos en venta mientras que los restantes no tienen tantos autos en venta comparado con estos 4. Además tenemos la siguiente gráfica sobre el color de los autos.

Los cuatro colores más populares son blanco, plata, negro y gris. Asimismo se graficó un histograma de precios respecto a cada compañía, esto para dar un panorama más amplio respecto a la distribución de los precios (y por ende sector del los consumidores) que tiene cada compañía
Con esta gráfica podemos ver que la mayoría de los autos tienen un costo bajo, lo cual tiene sentido ya que en general la mayoría de la población es de clase media/baja. Así, será más precisa la predicción para autos con un menor precio pues hay mayor cantidad de información para estos autos mientras que para autos costosos hay menos información por lo que las predicciones podrían ser menos fiables.

## Predicción
Se aplicaron dos algoritmos de la paquetería scikit-learn. Estos fueron LinearRegression y RandomForestRegressor. 
* Para LinearRegression se observa que hay una precisión de 60% tanto en los datos de entrenamiento como en los datos de prueba por lo que este algoritmo no es muy eficiente.
* Por otro lado, con RandomForestRegressor se obtuvo una precisión del 93% por lo que esta estimación es mucho más confiable. 

## Conclusiones
De la sección anterior podemos obtener una muy buena predicción para obtener el valor de un auto con dadas las características del conjunto de datos.