# 📊 Análisis de Churn - Telecom X

## Descripción

Este proyecto tiene como objetivo analizar el abandono de clientes (churn) en Telecom X, identificando patrones y factores que influyen en la decisión de cancelación del servicio. A través de un análisis exploratorio de datos, se busca proporcionar insights que permitan diseñar estrategias efectivas de retención.

---

## Índice

1. [Introducción](#introducción)
2. [Normalización, Limpieza y Tratamiento de Datos](#limpieza-y-tratamiento-de-datos)
3. [Análisis Exploratorio de Datos](#análisis-exploratorio-de-datos-eda)
4. [Conclusiones e Insights](#conclusiones-e-insights)
5. [Recomendaciones Estratégicas](#recomendaciones-estratégicas)
6. [Tecnologías Utilizadas](#tecnologías-utilizadas)
---

## Introducción

El análisis de churn es crucial para entender las razones detrás de la cancelación de servicios por parte de los clientes. Este estudio se centra en Telecom X, con el fin de identificar variables que correlacionan con una mayor tasa de evasión y proponer acciones que minimicen esta tendencia.

---

## Limpieza y Tratamiento de Datos

Se llevaron a cabo los siguientes pasos:

1. **Importación de datos**: Obtención de datos desde la API en formato JSON y conversión a DataFrame.
2. **Normalización de columnas**: Desanidado de columnas anidadas y creación de un diccionario para su interpretación.
3. **Renombrado de columnas**: Asignación de nombres en español y coherentes para facilitar su comprensión.
4. **Tratamiento de valores nulos**:

   * Reemplazo de valores en blanco en la columna `churn` por `"No se sabe"`.
   * Conversión de espacios en blanco en `total_charges` a `NaN` y posterior transformación a tipo numérico.
5. **Creación de columnas derivadas**: Cálculo de `Cuentas_Diarias` como `cargo_mensual / 30`, redondeado a dos decimales.
6. **Binarización de variables**: Conversión de columnas con valores "Yes"/"No" a `True`/`False`.
7. **Conversión de tipos de datos**: Ajuste de tipos a numérico, categórico y booleano según corresponda.

---

## Análisis Exploratorio de Datos

### 1️⃣ Resumen de Variables

* **Variables numéricas**: `cargo_mensual`, `cargo_total`, `antigüedad_meses`, `Cuentas_Diarias`.
* **Variables categóricas**: `género`, `tipo_contrato`, `método_pago`, entre otras.
* **Variables binarias**: `pareja`, `dependientes`, `adulto_mayor`, etc.

### 2️⃣ Distribución de Churn

Se observó que:

* **71.2%** de los clientes no cancelaron el servicio.
* **25.7%** cancelaron el servicio.
* **3.1%** no tienen información sobre su estado de churn.

### 3️⃣ Distribución de Churn según Variables Categóricas

Se analizaron variables como `tipo_contrato`, `método_pago` y `género`, encontrando que:

* Los clientes con **contratos mes a mes** tienen una mayor tasa de churn.
* Los clientes que utilizan **métodos de pago electrónicos específicos** presentan una mayor tasa de cancelación.

### 4️⃣ Distribución de Variables Numéricas según Churn

Se identificó que:

* Los clientes con **menor antigüedad** y **menor gasto total** tienen una mayor probabilidad de cancelar el servicio.

---

## Conclusiones e Insights

* **25% de los clientes han cancelado el servicio**, lo que representa una oportunidad significativa para mejorar la retención.
* Las variables **tipo de contrato** y **método de pago** son factores clave asociados al churn.
* Los clientes con **menor antigüedad** y **menor gasto total** son más propensos a abandonar el servicio.

---

## Recomendaciones Estratégicas

1. **Fidelización de clientes nuevos**: Implementar programas de retención dirigidos a clientes con contratos recientes.
2. **Revisión de métodos de pago**: Evaluar la efectividad de los métodos de pago utilizados y considerar alternativas que favorezcan la retención.
3. **Monitoreo de métricas clave**: Establecer indicadores de rendimiento que permitan identificar señales tempranas de churn y actuar proactivamente.

---

## Tecnologías Utilizadas

* **Python**: Análisis y procesamiento de datos.
* **Pandas y Numpy**: Manipulación de datos.
* **Matplotlib y Seaborn**: Visualización de datos.
* **Google Colab**: Documentación y presentación del análisis.

--
