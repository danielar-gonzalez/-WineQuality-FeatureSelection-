# -WineQuality-FeatureSelection-

En este proyecto se trabajó con la base de datos "Vino_Tinto.csv", que contiene 1,599 observaciones sobre vinos, con 11 características de entrada y una variable de salida, "calidad", que representa la calidad del vino según una escala del 0 al 10. Este conjunto de datos fue obtenido del UCI Machine Learning Repository y se encuentra originalmente en la revista Decision Support Systems. A través de este ejercicio, se aplicaron métodos de selección de características para determinar las variables más relevantes para predecir la calidad del vino.

Las **variables** disponibles en el conjunto de datos son:

- *acidezFija*: La acidez fija del vino, medida en gramos de ácido tartárico por decímetro cúbico.
- *acidezVolatil*: La acidez volátil del vino, medida en gramos de ácido acético por decímetro cúbico.
- *acidoCitrico*: Gramos de ácido cítrico por decímetro cúbico.
- *azucarResidual*: Gramos de azúcar por decímetro cúbico.
- *cloruros*: Gramos de cloruro de sodio por decímetro cúbico.
- *dioxidoAzufreLibre*: Miligramos de dióxido de azufre libre por decímetro cúbico.
- *dioxidoAzufreTotal*: Miligramos de dióxido de azufre total por decímetro cúbico.
- *densidad*: Medida en gramos por centímetro cúbico.
- *pH*: Valor del vino en la escala de pH.
- *sulfatos*: Gramos de sulfato de potasio por decímetro cúbico.
- *alcohol*: Volumen percentil de alcohol en el vino.
- *calidad*: Mediana de la calidad otorgada por al menos tres catadores, en una escala del 0 al 10.


**División de los datos**: Los datos fueron divididos en dos conjuntos: uno de entrenamiento (80%) y uno de prueba (20%), garantizando que la división fuera aleatoria para evitar sesgos en la evaluación del modelo.

**Selección hacia adelante**: Se aplicó el método de selección hacia adelante utilizando la librería mlxtend, con un rango de entre 2 a 8 variables seleccionadas. El modelo de regresión lineal se utilizó como estimador, y la métrica de rendimiento fue el R², con validación cruzada de 10 instancias.

**Selección hacia atrás**: A continuación, se realizó un proceso de selección hacia atrás sobre las variables seleccionadas en el paso anterior, con un rango de entre 2 a 5 variables. Este proceso tiene como objetivo eliminar las características menos significativas y reducir la complejidad del modelo.

**Entrenamiento y evaluación**: Se entrenaron los modelos resultantes utilizando solo las variables seleccionadas por ambos métodos. La capacidad predictiva de los modelos se evaluó usando la métrica R² sobre el conjunto de prueba.

**Comparación de modelos**: Se compararon los modelos obtenidos en los pasos anteriores, observando el desempeño de cada uno en cuanto al valor de R², para determinar cuál de las metodologías (selección hacia adelante o eliminación hacia atrás) resultó en un mejor modelo.


Documentos incluídos en el proyecto:
- [Reporte en formato ipynb](./caracteristicasVino.ipynb)
- [Reporte en formato html](./caracteristicasVino.html)
- [Base de datos](./Vino_Tinto.csv)
