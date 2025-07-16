# ChallengeDataScienceTelecomX
Challenge ONE Data Science – Telecom X

# 📊 Proceso ETL y Análisis Exploratorio – Churn de Clientes | Telecom X

Bienvenido/a al repositorio del **proceso ETL** (Extracción, Transformación y Carga) y **análisis exploratorio** de datos de churn de clientes para la empresa ficticia **Telecom X**.  
Aquí encontrarás el flujo completo: desde la obtención, limpieza y transformación de datos, hasta la visualización y análisis inicial de los factores relacionados con la evasión de clientes.

---

## 🚦 Tabla de Contenidos

- [1. Proceso ETL](#proceso-etl)
  - [📥 Extracción](#extracción)
  - [🧹 Transformación](#transformación)
  - [💾 Carga](#carga)
- [2. Análisis Exploratorio](#análisis-exploratorio)
- [3. Conclusiones](#conclusiones)
- [4. Archivos Generados](#archivos-generados)
- [5. Autor](#autor)

---

## 1. Proceso ETL

### 📥 Extracción

- **Lectura directa del archivo .json** desde un repositorio remoto de GitHub:  
  [TelecomX_Data.json](https://raw.githubusercontent.com/eD07/ChallengeDataScienceTelecomX/main/TelecomX_Data.json)

---

### 🧹 Transformación

- **Normalización de estructuras anidadas:**  
  - Columnas: `customer`, `phone`, `account`, `internet`.

- **Limpieza de datos:**  
  - Conversión de tipos de datos (`object` → `float`).
  - Eliminación de columnas redundantes.
  - Verificación y tratamiento de valores nulos y duplicados.

- **Renombramiento y creación de nuevas variables:**  
  - Ejemplo:  
    - `DailyCharges` = `ChargesMonthly` / 30

- **Conversión de variables categóricas a binarias:**  
  - Ejemplo: `"Yes" / "No"` → `1 / 0`

- **Estandarización de valores:**  
  - Limpieza y homogeneización de la columna `Churn` (`Yes` / `No`).
  - Mapeo numérico para `Contract`:  
    - `"Month-to-month"` → 1  
    - `"One year"` → 2  
    - `"Two year"` → 3

---

### 💾 Carga

- El DataFrame final procesado se guarda como:  
  `Churn_de_Clientes.json`

---

## 2. Análisis Exploratorio

### 🔘 Proporción de churn

- **Gráfico tipo torta** que muestra la proporción entre:
  - Clientes que permanecen
  - Clientes que se dieron de baja

### 🔥 Heatmap de características categóricas

- **Análisis cruzado de:**
  - **Eje Y:** Género + Tipo de contrato
  - **Eje X:** Tipo de servicio de internet
- **Visualización tipo semáforo:**  
  - Verde → baja evasión  
  - Rojo → alta evasión

### 📊 Variables numéricas

- **Boxplots comparativos para analizar:**
  - **ChargesMonthly:** Clientes que se dieron de baja tienden a tener gastos mensuales más altos.
  - **Tenure:** Clientes que permanecen tienen mayor antigüedad.

---

## 3. 📌 Conclusiones

- **Contratos a corto plazo, cargos mensuales elevados y baja antigüedad** se asocian fuertemente con la evasión de clientes.
- **El tipo de internet y la presencia de servicios de soporte** (como `TechSupport` y `OnlineSecurity`) influyen significativamente en la retención.
- Este análisis exploratorio sienta las bases para:
  - Modelos predictivos de churn.
  - Estrategias de retención de clientes.

---

## 4. 📁 Archivos Generados

- `Churn_de_Clientes.json` → Dataset procesado.
- `grafico_churn.png` → Gráfico de torta (churn).
- Otros gráficos y análisis visuales disponibles en la notebook principal.

---

## 5. 👨‍💻 Autor


- **Desarrollado por: Edgardo Encina Pino** 
- **Repositorio base: https://github.com/eD07/ChallengeDataScienceTelecomX**
  
---

## 🔗 Enlaces útiles
- [Python (descarga)](https://www.python.org/downloads/)
- [Jupyter Notebook](https://jupyter.org/install)
- [Google Colab](https://colab.research.google.com/)

