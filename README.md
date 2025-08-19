# 🚀 Telecom X: Predicción de Abandono (Churn)

## 📖 Tabla de Contenidos
- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Objetivos del Desafío](#-objetivos-del-desafío)
- [Estructura del Repositorio](#-estructura-del-repositorio)
- [Metodología de Análisis](#-metodología-de-análisis)
- [Hallazgos Clave y Conclusiones](#-hallazgos-clave-y-conclusiones)
- [Estrategias de Retención](#-estrategias-de-retención)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Cómo Usar el Proyecto](#-cómo-usar-el-proyecto)

## 📝 Descripción del Proyecto
Este proyecto es la segunda parte del desafío **Telecom X**, enfocado en la aplicación de **Machine Learning** para predecir la cancelación de clientes (Churn). Partiendo de un análisis de datos exploratorio (EDA) previo, el objetivo fue construir un pipeline robusto para entrenar y evaluar modelos predictivos.

La meta principal es identificar a los clientes con alta probabilidad de abandonar el servicio, permitiendo a la empresa tomar acciones proactivas para retenerlos.

## 🎯 Objetivos del Desafío
-   **Preprocesamiento de Datos:** Preparar el conjunto de datos para el modelado, incluyendo la limpieza, codificación de variables categóricas, manejo de desbalanceo de clases y normalización.
-   **Análisis de Variables:** Identificar las características más importantes para la predicción de Churn a través de análisis de correlación y la interpretación de los modelos.
-   **Modelado Predictivo:** Entrenar al menos dos modelos de clasificación (Regresión Logística y Random Forest) y evaluar su rendimiento con métricas clave.
-   **Conclusiones Estratégicas:** Proporcionar un informe con los factores más influyentes en el Churn y proponer estrategias de retención basadas en los resultados de los modelos.

## 📁 Estructura del Repositorio
-   `README.md`: Este archivo, que proporciona una visión general del proyecto.
-   `telecom_x_parte_2_alura.ipynb`: El cuaderno de Colab que contiene todo el código del pipeline de Machine Learning, desde el preprocesamiento hasta la evaluación de los modelos.
-   `df_limpo.csv`: El DataFrame limpio y listo para ser utilizado en el modelado.

## 🧠 Metodología de Análisis
El proyecto se desarrolló siguiendo un pipeline estructurado de Machine Learning:
1.  **Limpieza y Preprocesamiento:** Se eliminaron columnas irrelevantes, se aplicó *One-Hot Encoding* a las variables categóricas y se eliminaron los valores nulos e infinitos para asegurar la calidad de los datos.
2.  **Balanceo de Clases:** Se utilizó **SMOTE (Synthetic Minority Over-sampling Technique)** en el conjunto de entrenamiento para mitigar el desbalanceo entre las clases `No Churn` y `Churn`.
3.  **Normalización:** Se aplicó `StandardScaler` a los datos numéricos para asegurar un rendimiento óptimo en modelos sensibles a la escala, como la Regresión Logística.
4.  **Modelado Predictivo:** Se entrenaron y evaluaron dos modelos:
    * **Regresión Logística:** Un modelo lineal interpretable.
    * **Random Forest:** Un modelo robusto basado en árboles.
5.  **Evaluación y Conclusiones:** Se comparó el rendimiento de los modelos con métricas como la Matriz de Confusión, el *Recall* y el *ROC AUC* para extraer conclusiones estratégicas.

## 📊 Hallazgos Clave y Conclusiones
El análisis de la importancia de las variables reveló que los principales factores que impulsan el Churn son:
-   **Tiempo de contrato (`customer.tenure`):** La variable más crítica, indicando que los clientes con menor antigüedad son más propensos a cancelar.
-   **Tipo de contrato:** Los clientes con **contratos mensuales** tienen un riesgo de Churn mucho mayor que aquellos con contratos de largo plazo.
-   **Servicio de internet (`internet.InternetService_Fiber optic`):** La fibra óptica, a pesar de ser un servicio de alta gama, está fuertemente correlacionada con el Churn.
-   **Cargos totales (`account.Charges.Total`):** Los clientes con mayores gastos totales también muestran una mayor propensión a cancelar.

El modelo **Random Forest** demostró ser más preciso y robusto, especialmente en la identificación de los clientes que realmente abandonarán el servicio (alto *recall*), lo que lo convierte en una herramienta invaluable para la empresa.

## ✨ Estrategias de Retención
Basado en los hallazgos de los modelos, se proponen las siguientes acciones proactivas:
1.  **Programa de Bienvenida para Nuevos Clientes:** Implementar un programa de seguimiento intensivo en los primeros meses para construir lealtad.
2.  **Incentivos para Contratos a Largo Plazo:** Crear ofertas atractivas para migrar a contratos de uno o dos años, reduciendo el riesgo de Churn.
3.  **Análisis de la Calidad del Servicio de Fibra Óptica:** Investigar la causa de la alta tasa de cancelación en este segmento y ajustar la oferta.

## 🛠 Tecnologías Utilizadas
-   Python
-   Pandas
-   Scikit-learn
-   Matplotlib
-   Seaborn
-   Imblearn (para balanceo de clases)

## 🚀 Cómo Usar el Proyecto
1.  Clona este repositorio: `git clone https://aws.amazon.com/es/what-is/repo/`
2.  Abre el archivo `Notebook_Parte_2.ipynb` en Google Colab o Jupyter Notebook.
3.  Ejecuta cada celda en orden para replicar el análisis y los modelos.

---
