# Parcial-1
 Predecir el Monto Total (Facturacion) que un Usuario Pagara en el Proximo Mes
Predicción del Costo Total en TelcoAndes 📊
Proceso de Minería de Datos 🛠️
El objetivo de este proyecto fue predecir el monto total que un usuario de TelcoAndes pagará en el próximo mes. Esto incluye tanto la tarifa fija del plan (costo mensual) como los cargos adicionales por llamadas, SMS y datos que exceden los límites del plan. A continuación, se detallan los pasos realizados para procesar y analizar los datos:

1. Análisis Exploratorio de Datos (EDA) 📈
En esta etapa, se exploraron y analizaron los datos para entender su calidad, identificar posibles problemas y descubrir patrones interesantes:

Se revisaron los tipos de variables, rangos de valores y valores faltantes en los datos.
Se identificaron posibles outliers en los datos de consumo (por ejemplo, llamadas excesivas, uso elevado de datos, etc.).
Se crearon visualizaciones básicas como histogramas y boxplots para observar la distribución de las variables, especialmente el costo total de los usuarios y sus relaciones con características demográficas (edad, región, género).
2. Data Wrangling (Limpieza de Datos) 🧹
Una vez que se entendió el conjunto de datos, se realizó la limpieza para garantizar que estuviera listo para el análisis y modelado:

Manejo de valores faltantes: Se verificaron los valores faltantes y se tomaron decisiones sobre cómo tratarlos (eliminación o imputación).
Identificación de outliers: Se detectaron y trataron los outliers en los consumos (llamadas extremas, SMS excesivos, sobreuso de datos) para evitar que distorsionaran el modelo.
Unificación de tablas: Se combinaron las tres tablas principales (Usuarios, Planes y Consumos) mediante joins apropiados para formar un solo dataset que se pudiera utilizar para entrenar el modelo. Durante este paso, se cuidó la duplicación de registros y se resolvieron inconsistencias.
3. Feature Engineering 🔧
El siguiente paso fue la creación de nuevas variables para mejorar la capacidad predictiva del modelo:

Se generaron variables como total_calls, total_sms, total_mb y extra_usage, que ayudaron a capturar mejor el comportamiento del usuario respecto a los consumos.
Se aplicaron transformaciones a algunas variables originales, como log-transform y escalado, para mejorar la relación entre las variables y la predicción.
Se incluyeron variables demográficas como edad, género y región, que se consideraron importantes para el modelo.
4. Entrenamiento y Evaluación de Modelos de Regresión 🎯
Con los datos procesados y las características creadas, se dividió el dataset en dos partes: entrenamiento y prueba. Luego, se entrenaron diferentes modelos de regresión para predecir el costo total del usuario en el siguiente mes:

Se entrenaron varios modelos de regresión, como Regresión Lineal, Gradient Descent y Stochastic GD.
Se evaluaron los modelos utilizando métricas de error como RMSE, MAE y R² para determinar cuál de ellos proporcionaba las mejores predicciones.
Finalmente, se seleccionó el modelo de Regresión Lineal como el mejor para predecir el costo total debido a su desempeño relativamente bueno en las métricas de error, aunque con un R² bajo.
Conclusión 🏁
El proceso de minería de datos permitió realizar una predicción bastante útil sobre el costo total que un usuario podría pagar en el próximo mes. Aunque el modelo de Regresión Lineal no alcanzó un R² muy alto (0.0057), los resultados siguen siendo valiosos para crear estrategias comerciales y ofrecer servicios personalizados a los usuarios. Este modelo puede ser utilizado para ayudar a TelcoAndes a ajustar sus precios, ofertas y promociones.

Mejoras a Futuro
Para mejorar los resultados y las predicciones futuras, se podrían considerar las siguientes acciones:

Incorporar más datos de otros servicios o más tiempo de consumo para una mayor precisión.
Probar con modelos más complejos como XGBoost o Random Forest.
Segmentar a los usuarios utilizando técnicas de clustering, lo que permitiría personalizar aún más las estrategias de marketing.
En resumen, este análisis proporciona una base sólida para futuras predicciones y decisiones estratégicas en TelcoAndes. ¡Vamos hacia un futuro de predicciones más precisas! 🚀


Instrucciones para Ejecutar el Proyecto
Clona el repositorio:
git clone <URL del repositorio>

Instala las dependencias:
pip install -r requirements.txt
