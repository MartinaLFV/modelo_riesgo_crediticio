# modelo_riesgo_crediticio
Modelo de riesgo crediticio (PD – Probability of Default) con dataset público de Kaggle. Incluye análisis exploratorio de variables, preprocesamiento con PdE/WOE, regresión logística (Accuracy 85%, AUC 0.87) y construcción de scorecard tipo FICO (300-850) para evaluar e interpretar riesgo.


Riesgo Crediticio - Modelo de Probabilidad de Default (PD)
Descripción del Proyecto

Este proyecto implementa un modelo de Probabilidad de Default (PD) utilizando regresión logística para predecir el riesgo crediticio de clientes.
Incluye todo el flujo de trabajo: desde el preprocesamiento de datos, estimación y validación del modelo, hasta la construcción de scorecards y un predictor interactivo para evaluar clientes individuales.

El objetivo es apoyar la toma de decisiones crediticias y facilitar la interpretación de los riesgos asociados a cada cliente.

Tecnologías y Librerías
Python 3.x
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn (LogisticRegression, métricas de evaluación)
Category_encoders
XGBoost, LightGBM, CatBoost (importados para posibles comparaciones)
Google Colab y Google Drive para almacenamiento y carga de datasets
Widgets de Jupyter para predictor interactivo

Flujo del Proyecto
1. Carga de datos
Se cargan los datasets de entrenamiento y evaluación desde Google Drive.

3. Preprocesamiento
Selección de variables relevantes por categoría.
Creación de variables dummies y definición de categorías de referencia.

3. Estimación del modelo
Regresión logística con sklearn.
Cálculo de coeficientes e intercepto.
Estimación de p-values para determinar significancia estadística de las variables.

4. Validación del modelo
Matriz de confusión (absoluta y porcentual).
Métricas de desempeño:
Exactitud (accuracy)
AUC (Area Under ROC Curve)
Coeficiente de Gini
Estadístico K-S

Visualizaciones:
Curva ROC
Curva de Lorenz / Gini
Curva K-S

5. Scorecards
Transformación de coeficientes a un puntaje crediticio entre 300 y 850.
Cálculo de puntajes individuales para clientes de evaluación.
Ajuste de intercepto y escalado para mayor interpretabilidad.

6. Punto de corte y decisiones crediticias
Evaluación de diferentes puntos de corte usando la curva ROC.
Cálculo de tasas de aprobación y rechazo según punto de corte seleccionado.

7. Predictor interactivo
Widget que permite seleccionar características de un cliente.
Devuelve:
Probabilidad de default
Predicción binaria (DEFAULT / NO DEFAULT)
Permite evaluar clientes hipotéticos de manera intuitiva.

Resultados del Modelo
AUC: 0.8698 → Muy bueno, el modelo discrimina correctamente entre clientes buenos y malos.
Accuracy: 85% → Muy bueno
Gini: 0.7396 → Capacidad de discriminación sólida.
