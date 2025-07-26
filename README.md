# telecomX2-jddc

# Análisis de Cancelación de Clientes

Este cuaderno de Google Colab documenta un proyecto de análisis predictivo enfocado en identificar los factores que influyen en la cancelación de clientes y construir modelos para predecir la probabilidad de que un cliente cancele su servicio.

## Contenido del Cuaderno

El cuaderno está organizado en las siguientes secciones principales:

1.  **Preparación de los Datos:** Carga del conjunto de datos, limpieza inicial, eliminación de columnas irrelevantes y codificación de variables categóricas (One-Hot Encoding).
2.  **Análisis de Desbalance de Clases:** Verificación de la proporción de clientes que cancelan versus los que no cancelan y evaluación del desbalance.
3.  **Balanceo de Clases (SMOTE):** Aplicación de la técnica SMOTE (Synthetic Minority Over-sampling Technique) para abordar el desbalance de clases y mejorar el rendimiento del modelo en la clase minoritaria.
4.  **División de Datos:** Separación del conjunto de datos balanceado en conjuntos de entrenamiento y prueba para el desarrollo y evaluación del modelo.
5.  **Análisis Exploratorio y Visualización:** Investigación de las relaciones entre variables clave y la cancelación mediante matrices de correlación y gráficos (boxplots, scatter plots).
6.  **Modelado Predictivo:** Entrenamiento de varios modelos de clasificación (Regresión Logística, Árbol de Decisión, Bosque Aleatorio, Gradient Boosting) en el conjunto de entrenamiento.
7.  **Evaluación de Modelos:** Evaluación del rendimiento de cada modelo utilizando métricas estándar (Exactitud, Precisión, Recall, F1-score) y matrices de confusión.
8.  **Análisis de Importancia de Variables:** Identificación de las variables más relevantes para la predicción de la cancelación según cada modelo entrenado.
9.  **Interpretación y Conclusiones:** Resumen de los hallazgos clave, identificación de los principales factores de cancelación y propuesta de estrategias de retención basadas en los resultados del análisis y los modelos.

## Cómo Ejecutar el Cuaderno

1.  Abre el cuaderno en Google Colab.
2.  Asegúrate de que el archivo de datos `datos_tratados.csv` esté disponible en la ruta `/content/datos_tratados.csv` en tu entorno de Colab. Puedes subirlo si es necesario.
3.  Ejecuta las celdas del cuaderno secuencialmente, de arriba a abajo. Cada sección se basa en los resultados de las secciones anteriores.
4.  Observa los resultados de las celdas de código y las visualizaciones para seguir el proceso de análisis y modelado.

## Hallazgos Principales

Los factores que más influyen en la cancelación identificados en este análisis incluyen:
*   Tiempo de contrato (tenure)
*   Gasto mensual y total
*   Tipo de servicio de internet (Fibra Óptica)
*   Método de pago (Cheque Electrónico)
*   Tipo de contrato (mes a mes vs. a largo plazo)
*   Adopción de servicios adicionales

El modelo de **Bosque Aleatorio** y **Gradient Boosting** mostraron el mejor rendimiento predictivo en este conjunto de datos después de aplicar SMOTE.

## Estrategias de Retención Propuestas

Las estrategias de retención sugeridas se centran en abordar los factores clave identificados, como enfocarse en clientes de corto plazo, revisar servicios de alto costo/fibra óptica, promover métodos de pago automáticos y contratos a largo plazo, y destacar el valor de los servicios adicionales.
