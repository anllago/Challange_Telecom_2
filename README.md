# 📊 Análisis de Evasión de Clientes – Telecom X

## 🔹 Descripción
Este proyecto analiza la **evasión de clientes (churn)** en Telecom X, identificando factores que influyen en la pérdida de clientes y proponiendo estrategias de retención.

---

## 📁 Estructura del Proyecto
- `notebooks/` : Análisis exploratorio y visualizaciones.  
- `scripts/` : Limpieza, transformación y preparación de datos.  
- `data/` : Datos de clientes (JSON/CSV).  

---

## 🛠 Tecnologías y Librerías
- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE, NearMiss)  

---

## ⚙️ Flujo de Trabajo
1. **Extracción y limpieza de datos**  
   - Normalización de datos anidados (`pd.json_normalize`).  
   - Eliminación de valores vacíos y creación de nuevas columnas (`Cuentas_Diarias`).  
   - Conversión de `Churn` a binario y renombramiento de columnas al español.  

2. **Análisis Exploratorio de Datos (EDA)**  
   - Distribución de churn y visualización de variables categóricas y numéricas.  
   - Identificación de variables más relevantes: **Tiempo como cliente**, **Tipo de contrato**, **Cuenta total**.  

3. **Preparación de Datos para Modelado**  
   - Codificación de variables categóricas (`OneHotEncoder`).  
   - Oversampling y undersampling (SMOTE y NearMiss).  
   - Normalización de variables (`MinMaxScaler`).  

4. **Modelado Baseline y Validación**  
   - DummyClassifier como punto de referencia.  
   - Validación cruzada estratificada (`StratifiedKFold`).  

---

## 📌 Hallazgos Principales
- La tasa de evasión promedio es **26.5%**.  
- Clientes nuevos o con contratos a corto plazo presentan mayor riesgo de churn.  
- El método de pago y la cantidad de servicios contratados influyen en la probabilidad de abandono.  

---

## 💡 Recomendaciones Estratégicas
1. Incentivar contratos a largo plazo (1 o 2 años).  
2. Ofrecer paquetes promocionales que aumenten el gasto mensual.  
3. Premiar la lealtad de clientes con más de 1 año de antigüedad.  

---

## 📊 Visualizaciones
- Barras y pastel de distribución de churn.  
- Boxplots y KDE plots para variables numéricas vs. evasión.  
- Heatmap de correlaciones entre variables.

---
