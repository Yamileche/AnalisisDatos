# Predicción de consultas en una página web
En esta ocasión se analizará un set de datos de una página web escolar, el set de datos cuenta con un historial de 5 años de información diaria, se tiene la siguiente información:
* Cantidad de veces que la página es cargada
* Visitas únicas
* Página visitada por primera vez
* Veces que se regresó a ver la página web

El set de datos puede consultarse en el siguiente link: https://www.kaggle.com/datasets/bobnau/daily-website-visitors. Cabe aclarar que cada usuario en la visita es considerando la IP por lo que si se realizan conexiones desde la mima IP se considera como un mismo usuario.

El objetivo del análisis es encontrar un patrón en las visitas para así entender el comportamiento de el ingreso de los estudiantes en el sitio web. De esta forma se podrían modificar los servidores para un mejor soporte a los usuarios. 

## Análisis
Antes de comenzar con un análisis sobre el comportamiento de las visitas, veamos un mapa relacional de las variables del set de datos:
De lo anterior vemos que hay una estrecha relación entre las variables por lo que es muy posible que se comporten de forma muy similar. 

Aquí vemos que hay una patrón anual donde al iniciar el año se sube el número de cargas diarias, a mitad del año bajan las cargas sin embargo se mantiene la cantidad de cargas en un nivel bajo para luego volver a subir y al final del año hay un descenso de las cargas muy abrupto y luego sube inmediatamente al inicio del año. Lo anterior puede explicarse por el periodo de exámenes finales al terminal el semestre además que durante vacaciones de verano los estudiantes siguen estudiando sin embargo en las vacaciones de fin de año los estudiantes cesan los estudios.  El patrón anterior se confirma con la gráfica de la superposición anual de los datos.

Aquí se observa claramente el patrón de comportamiento de las cargas a lo largo del año, se observa que tiene una tendencia periódica por lo que se puede intentar una predicción utilizando funciones trigonométricas, para esto se utiliza CalendarFourier. Aplicando una regresión lineal se obtiene la siguiente predicción:
De lo anterior se tiene una estimación bastante buena en el comportamiento de los datos. 

Por la parte anual se ha logrado encontrar un patrón  en la cantidad de cargas a la pagina web, sin embargo también es de interés encontrar un patrón semanal, se puede observar que hay un aumento claro en el número de cargas en los días laborales. 

## Conclusión
Con el análisis anterior se logró encontrar un patrón en el comportamiento de los datos así como una predicción bastante buena en el comportamiento de los datos tanto de forma anual tanto semanal. 

Con la información restante (Visitas únicas, Visitado por primera vez, Visitado nuevamente) hay un patrón muy similar en el comportamiento de la información por lo que basta con repetir el proceso para encontrar patrones y predicciones similares.