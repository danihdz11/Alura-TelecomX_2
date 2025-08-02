# 📊 Predicción de Cancelación de Clientes (Churn) – Proyecto Telecom X

Este repositorio contiene un análisis completo orientado a predecir la **cancelación de clientes (churn)** en una empresa de telecomunicaciones. A través de un enfoque supervisado de aprendizaje automático, se desarrollaron modelos predictivos basados en variables del comportamiento y características contractuales de los usuarios.

---

## Objetivo del proyecto

El propósito principal es **identificar los factores clave asociados a la cancelación** de clientes y construir modelos predictivos capaces de anticipar el churn. Esto permite a la empresa tomar decisiones más informadas en sus estrategias de retención.

---

## Preparación de los Datos

### Clasificación de variables:
- **Categóricas**: género, tipo de contrato, método de pago, servicios activos, etc.
- **Numéricas**: tenure, monthly charges, total charges, total de servicios, etc.

### Etapas realizadas:
- **Limpieza de datos**: eliminación de columnas no predictivas como `customerID`.
- **Codificación One-Hot** para variables categóricas.
- **Balanceo de clases** con **SMOTE** debido a un desbalance de ~73% clientes activos vs ~27% cancelaciones.
- **División del dataset** en 80% entrenamiento y 20% prueba con `train_test_split()`.

---

## Modelado y justificaciones

Se aplicaron dos modelos principales:

1. **Regresión Logística**  
   - Requiere normalización. Permite interpretar coeficientes directamente.
   - Ideal para establecer relaciones lineales entre las variables y el churn.

2. **Random Forest**  
   - No requiere normalización. Se enfoca en la capacidad predictiva.
   - Útil para evaluar la importancia relativa de cada variable.

### Decisiones tomadas:
- No se aplicó normalización global, ya que uno de los modelos elegidos (Random Forest) no la requiere.
- Se balancearon los datos solo en el conjunto de entrenamiento, para evitar data leakage.

---

## Exploración de Datos (EDA)

Se generaron visualizaciones clave:

- 📌 **Matriz de correlación**: para identificar relaciones fuertes con `Churn`.
- 📌 **Boxplots**: `tenure` vs `Churn`, `TotalCharges` vs `Churn`.
- 📌 **Importancia de variables**: coeficientes en regresión logística y feature importance en Random Forest.


