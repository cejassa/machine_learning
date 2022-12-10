# PROYECTO_MACHINE_LEARNING
Estudio sobre la predicción de abandono de clientes.

El proyecto se ha realizado a través de los datos de una empresa real. El objetivo era predecir los clientes que se habían dado de baja durante el tiempo de vida de la empresa. 
Para ello se utilizaron 3 archivos CSV sacados del back office de la empresa (Django), Hubspot y ProfitWell, trabajando con miles de datos, limpiándolos y filtrándolos hasta quedarnos con un total de 2550 clientes y 7 variables:
- Antiguedad del cliente en la empresa
- Tiempo pasado desde que realizó el último registro
- Ingreso total a lo largo de su vida como cliente
- Nº tickets o incidencias asociadas
- Nº de propiedades 
- Total de check-ins o registros realizados
- Estado en la empresa (baja o activo)

Para hacer la predicción, se crearon diferentes modelos de clasificación:
- Gradient Boosting, Decision Tree, KNN, Ada Boost, Logistic Regression, Random Forest e incluso una red neuronal, siendo el SVC con un grid el que obtuvo mejor métrica de recall para los siguientes parámetros: C=1, coef0=10, kernel='sigmoid', con un total de 88% de score.
