# PROYECTO MACHINE LEARNING

Estudio sobre la **predicción de abandono de clientes**.
El proyecto se ha realizado a través de los datos de una **empresa real**. 

El objetivo era predecir si los nuevos clientes se van a dar de baja o no.
Para ello se utilizaron 3 archivos CSV sacados del back office de la empresa **(Django), Hubspot y ProfitWell**, trabajando con miles de datos, limpiándolos y filtrándolos hasta quedarnos con un total de **2550 clientes y 7 variables**:
- Antiguedad del cliente en la empresa
- Tiempo pasado desde que realizó el último registro
- Ingreso total a lo largo de su vida como cliente
- Nº tickets o incidencias asociadas
- Nº de propiedades 
- Total de check-ins o registros realizados
- Estado en la empresa (baja o activo)

![image](https://user-images.githubusercontent.com/110189994/213913253-8f7cadac-6e41-4a19-9f60-3b8eb767e453.png)

Para hacer la predicción, se **balancearon** las muestras, se **escalaron** los datos y se crearon diferentes **modelos de clasificación**:
- Gradient Boosting, Decision Tree, KNN, Ada Boost, Logistic Regression, Random Forest e incluso una red neuronal, siendo el SVC con un GridCV el que obtuvo mejor métrica de recall para los siguientes parámetros: C=1, coef0=10, kernel='sigmoid', con un total de 88% de score.

A pesar de eso, el modelo escogido fue el **Decision Tree**, con un 83% de recall, debido a que es un modelo de **caja blanca** que ayuda a comprender los resultados y poder aplicar una solución al problema de abandono de clientes.

![image](https://user-images.githubusercontent.com/110189994/213913103-3ed12290-26ce-4110-b526-a70c874493ce.png)

Conclusión: Se pudo concluir que las variables más predictivas eran el **tiempo sin uso y la antigüedad**, lo que puede indicar que al ser un software que da soporte a clientes con negocios turísticos, el motivo de baja puede ser causa del **cese del servicio post-vacacional** y no a algún tipo de problema técnico o falta de soporte.
