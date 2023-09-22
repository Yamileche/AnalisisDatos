# Análisis de calidad de vida dado poder adquisitivo, sueldo promedio y costo de vida

A continuación se detallará un análisis de un data set obtenido de kaggle que involucra poder adquisitivo, sueldo promedio y costo de vida de una serie de países de todo el mundo. El objetivo de este análisis es determinar, dado los índices anteriores, qué país tiene la mejor calidad de vida. La fuente del data set es: https://www.kaggle.com/datasets/meeratif/global-income-purchasing-power 
## Descripción del data set
Aquí hay una descripción de cada una de las columnas:

**Rank:** esta columna representa la clasificación de países o regiones según un criterio específico, que no se menciona explícitamente en el nombre de la columna. La clasificación podría estar relacionada con el costo de vida general, la calidad de vida, los indicadores económicos o cualquier otra métrica relevante. Los rangos más bajos suelen indicar un mejor rendimiento o costos más bajos, según el contexto.

**Country/Region:** esta columna contiene los nombres de los países o regiones que se analizan en el conjunto de datos. Cada fila corresponde a un país o región específica y esta columna sirve como identificador para cada punto de datos.
Cost Index: la columna del índice de costos proporciona un valor numérico que cuantifica el costo de vida en cada país o región. Un valor más alto del índice de costos indica que los gastos de manutención, como vivienda, comida, transporte y otros elementos esenciales, son relativamente altos en ese lugar en particular. Por el contrario, un índice de costo más bajo sugiere un costo de vida más asequible.

**Monthly Income:** Esta columna representa el ingreso mensual promedio de los residentes de cada país o región. Proporciona información sobre el potencial de ingresos y los niveles de ingresos de la población en diferentes áreas. Un ingreso mensual más alto generalmente sugiere mayores recursos financieros para los residentes.

**Purchasing Power Index:** la columna del índice de poder adquisitivo mide el poder adquisitivo relativo de la población en cada país o región. Indica hasta dónde llegará un ingreso determinado en términos de compra de bienes y servicios en ese lugar. Un índice de poder adquisitivo más alto sugiere que la población puede permitirse un nivel de vida relativamente más alto, mientras que un índice más bajo implica un poder adquisitivo reducido.

## Descripción del análisis
Dado lo anterior, como los valores de cada tabla no están normalizados, el primer paso es normalizar el cada columna. Seguido de lo anterior, se pretende otorgar un peso a cada columna, estos se pueden dar según se consideré necesario, para este análisis se proponen estos pesos
- Poder adquisitivo = 0.4
- Sueldo promedio = 0.3
- Costo de vida = 0.4

Con los pesos anteriores, como cada elemento está normalizado, solo basta multiplicar cada columna con su respectivo peso, luego para obtener el índice de calidad de vida se suman los valores anteriores (respecto a cada fila) y obtenemos el índice de calidad de vida.

## Conclusiones
Con el análisis anterior se concluye que Bermuda tiene el mejor índice de calidad de vida, seguido por Norway, Switzerland y Luxembourg.