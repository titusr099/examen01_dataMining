# Predicción de Facturación de Usuarios

Este proyecto tiene como objetivo desarrollar un modelo de predicción que estime la facturación mensual de los usuarios en función de su consumo de llamadas, mensajes y datos móviles. Los resultados pueden ser utilizados para optimizar estrategias de precios, promociones y retención de clientes.

## 1. Estructura del Proyecto

El proyecto está dividido en las siguientes etapas:

### 1.1 Exploración y Limpieza de Datos
- Análisis exploratorio de datos (`EDA`).
- Conversión de formatos de fecha y manejo de valores nulos.
- Agrupación de datos por usuario y mes.

### 1.2 Modelado y Feature Engineering
- Creación del esquema estrella (`Star Schema`) con tablas de hechos y dimensiones.
- Transformaciones matemáticas como `log-transform` y escalado con `StandardScaler`.

### 1.3 Entrenamiento y Evaluación de Modelos
- Se entrenaron y evaluaron distintos modelos de regresión:
  - **Regresión Lineal**
  - **S Gradient Descent (SGDRegressor)**
- Ambos modelos obtuvieron métricas similares.

### 1.4 Conclusiones y Recomendaciones de Negocio
- Interpretación de los resultados y su impacto en la estrategia comercial.
- Identificación de mejoras y posibles optimizaciones futuras.

---

## 2. Datos y Preprocesamiento

Los datos provienen de registros de consumo de usuarios de telefonía, organizados en los siguientes archivos:

- `megaline_calls.csv` -> Registros de llamadas realizadas por los usuarios. 
- `megaline_messages.csv` -> Registros de mensajes enviados. 
- `megaline_internet.csv` -> Datos de consumo de internet. 
- `megaline_users.csv` -> Información demográfica y plan de cada usuario. 
- `megaline_plans.csv` -> Características de los planes de telefonía. 


## 3. Modelos Evaluados y Resultados

Se compararon dos modelos principales de regresión:

Modelo - MSE - MAE - R² 

**Regresión Lineal** | 0.1301 | 0.3055 | 0.8661 |

**Gradient Descent (SGD)** | 0.1300 | 0.3052 | 0.8662 |

Ambos modelos lograron **resultados equivalentes**, por lo que se seleccionó **Regresión Lineal** debido a su menor costo computacional en datasets pequeños.


## 5. Instalación y Uso

### 5.1 Instalación de Dependencias
Ejecuta el siguiente comando para instalar todas las librerías necesarias:
pip install -r requirements.txt

Para ejecutar los notebooks del proyecto, inicia Jupyter Notebook con:
jupyter notebook


Autor: Roberth Lara
Fecha: 28/feb/2025