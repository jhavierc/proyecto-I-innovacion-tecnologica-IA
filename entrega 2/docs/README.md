# Entrega 2 - Proyecto I de Innovación Tecnológica
## Maestría en Inteligencia Artificial Aplicada - Universidad ICESI

---

## 📋 Resumen Ejecutivo

Esta entrega constituye la primera fase del **Proyecto I de Innovación Tecnológica** del programa de Maestría en Inteligencia Artificial Aplicada de la Universidad ICESI. El proyecto se enfoca en el desarrollo de soluciones tecnológicas innovadoras utilizando técnicas de inteligencia artificial para abordar problemas del mundo real.

### Objetivos de la Entrega

La segunda entrega tiene como objetivo establecer un análisis exploratorio de los datos y selección de modelos de referencia y experimentos para lograr resolver el planteamiento de la hipotesis del presente proyecto:

1. **[🎯 Análisis exploratorio de los datos](../src/data/preprocess.ipynb)**: Calidad de la exploración y justificación de la selección de los datos y variables.
2. **[📚 Modelos de referencia y experimentos](../src/models/)**: Implementación y evaluación de modelos de series temporales para predicción de capacidad energética
3. **[⚙️ Funciones reutilizables](../src/utils/funcions.ipynb)**: Biblioteca de funciones utilitarias para carga, preprocesamiento, visualización y evaluación de modelos  

---

## 🗂️ Navegación del Proyecto

### 📖 Documentos Principales

| Documento | Descripción | Estado |
|-----------|-------------|--------|
| **[📊 Análisis Exploratorio de Datos](../src/data/preprocess.ipynb)** | Análisis exploratorio, preprocesamiento e imputación de datos | ✅ Completado |
| **[📚 Modelos de Referencia](../src/models/)** | Implementación de modelos de series temporales (ARIMA, suavización, promedios móviles) | 🔄 En progreso |
| **[⚙️ Funciones Reutilizables](../src/utils/funcions.ipynb)** | Biblioteca de funciones utilitarias para el proyecto | ✅ Completado |

### 🔗 Enlaces Rápidos

- **[📊 Análisis Exploratorio de Datos](../src/data/preprocess.ipynb)** - Notebook de preprocesamiento y análisis de datos
- **[📚 Modelos de Series Temporales](../src/models/)** - Notebooks de modelado y experimentos
- **[⚙️ Funciones Reutilizables](../src/utils/funcions.ipynb)** - Biblioteca de funciones utilitarias
- **[⚙️ Instalación y Configuración](instalacion.md)** - Guía de instalación y dependencias
- **[📁 Estructura del Proyecto](../../estructura_proyecto.md)** - Organización de archivos y carpetas

---

## 🎯 Resumen de Objetivos

### 1. Análisis Exploratorio de Datos
**Objetivo**: Realizar un análisis completo de los datos de capacidad acumulada de energía renovable (Solar, Eólica, PCH) para entender su estructura, calidad y características.

**Contenido del Notebook**:
- Carga y exploración inicial de datos
- Imputación de valores faltantes (múltiples métodos)
- Estadísticas descriptivas
- Análisis de correlación
- Visualización de series temporales
- Análisis de residuos y normalidad
- Detección de outliers

[📖 Ver notebook de análisis →](../src/data/preprocess.ipynb)

### 2. Modelos de Referencia y Experimentos
**Objetivo**: Implementar y evaluar diferentes modelos de series temporales para predecir la capacidad acumulada de energía renovable (Solar) en Colombia.

**Notebooks de Modelado**:

| Notebook | Descripción | Estado |
|----------|-------------|--------|
| **[1_linear_regression.ipynb](../src/models/1_linear_regression.ipynb)** | Modelo de regresión lineal para análisis de tendencias en series temporales | ⏳ Pendiente |
| **[2_moving_averages.ipynb](../src/models/2_moving_averages.ipynb)** | Implementación de promedios móviles y suavización exponencial (Simple, Holt, Holt-Winters) para análisis de series temporales | ✅ Completado |
| **[3_time_series_smoothing.ipynb](../src/models/3_time_series_smoothing.ipynb)** | Análisis de suavización exponencial con descomposición estacional y comparación de métodos de suavización | ✅ Completado |
| **[4_time_series_regression.ipynb](../src/models/4_time_series_regression.ipynb)** | Modelos de regresión aplicados a series temporales | ⏳ Pendiente |
| **[5_time_series_arima.ipynb](../src/models/5_time_series_arima.ipynb)** | Modelo ARIMA con selección automática de parámetros (auto_arima) para predicción de capacidad de energía solar | ✅ Completado |

**Técnicas Implementadas**:
- Promedios móviles (MA) con diferentes ventanas
- Suavización exponencial simple
- Suavización exponencial lineal (Holt)
- Suavización exponencial con estacionalidad (Holt-Winters)
- Modelos ARIMA (Auto-Regressive Integrated Moving Average)
- Descomposición de series temporales (tendencia, estacionalidad, residuos)
- Evaluación de modelos con métricas de error (MSE, RMSE)

[📁 Ver carpeta de modelos →](../src/models/)


### 3. Funciones Reutilizables
**Objetivo**: Proporcionar una biblioteca centralizada de funciones utilitarias que faciliten el trabajo con datos de energía renovable en todo el proyecto, promoviendo la reutilización de código y la consistencia en el procesamiento.

**Ubicación**: [`../src/utils/funcions.ipynb`](../src/utils/funcions.ipynb)

**Categorías de Funciones**:

#### 📥 Carga y Preprocesamiento de Datos
| Función | Descripción |
|---------|-------------|
| `load_capacidad_data()` | Carga archivos CSV con formato específico del proyecto (delimitador `;`, decimal `,`) y convierte fechas |
| `load_capacidad_csv_data()` | Carga archivos CSV sin conversión automática de fechas |
| `preprocess_capacidad_data()` | Agrega características temporales (año, mes, día, día del año) al DataFrame |
| `extract_first_day_per_month()` | Extrae el primer día disponible de cada mes para reducir el tamaño del dataset |
| `impute_missing_values()` | Imputa valores faltantes usando múltiples métodos (forward fill, backward fill, interpolación lineal/polinomial/spline, media, mediana, KNN) |
| `compare_imputation_methods()` | Compara diferentes métodos de imputación y muestra estadísticas comparativas |

#### 📊 Visualización
| Función | Descripción |
|---------|-------------|
| `plot_time_series()` | Genera gráficos de series temporales para una o múltiples columnas |
| `plot_correlation_matrix()` | Crea una matriz de correlación visual con heatmap |
| `graph_moving_averages()` | Visualiza múltiples promedios móviles en una matriz de subplots |

#### 📈 Métricas de Evaluación
| Función | Descripción |
|---------|-------------|
| `calculate_metrics()` | Calcula métricas de evaluación para modelos de regresión (MSE, RMSE, MAE, R², MAPE) |
| `print_metrics()` | Imprime métricas de evaluación de forma formateada y legible |

#### 🔧 Utilidades Generales
| Función | Descripción |
|---------|-------------|
| `get_data_info()` | Muestra información resumida del DataFrame (forma, tipos, valores faltantes, estadísticas) |
| `save_results()` | Guarda DataFrames en formato CSV con el formato estándar del proyecto |

**Uso en el Proyecto**:
```python
# Importar funciones en cualquier notebook
%run ../utils/funcions.ipynb

# Ejemplo de uso
df = load_capacidad_data('../data/capacidad_acumulada.csv')
df_reduced = extract_first_day_per_month(df)
df_imputed = impute_missing_values(df_reduced, method='linear')
plot_time_series(df_imputed, columns=['SOLAR', 'EOLICA', 'PCH'])
```

**Ventajas**:
- ✅ Código reutilizable y consistente en todo el proyecto
- ✅ Reducción de duplicación de código
- ✅ Facilita el mantenimiento y actualización de funciones comunes
- ✅ Documentación integrada con docstrings completos
- ✅ Validación y manejo de errores centralizado

[📖 Ver notebook de funciones →](../src/utils/funcions.ipynb)

---

## 🛠️ Tecnologías y Herramientas

### Stack Tecnológico Principal
- **Backend**: Python 3.8+
- **Machine Learning**: Scikit-learn, Pandas, NumPy

### Herramientas de Desarrollo
- **Control de Versiones**: Git, GitHub
- **Testing**: pytest, Jest, Cypress

---

## Equipo (Roles ASUM-DM)

- **Project Manager**: Carlos Javier Cepeda - [carlos.cepeda@icesi.edu.co]
- **Business Analyst**: [Nombre] - [email@icesi.edu.co]
- **Data Scientist**: [Nombre] - [email@icesi.edu.co]
- **Data Engineer**: [Nombre] - [email@icesi.edu.co]
- **ML Engineer**: [Nombre] - [email@icesi.edu.co]

### Canales de Comunicación
- **Reuniones semanales**: Sabados 2:00 PM
- **Repositorio**: [https://github.com/jhavierc/proyecto-I-innovacion-tecnologica-IA]
- **Documentación**: [https://drive.google.com/drive/u/0/folders/1Db8Tqb3cyBQAeAQTrTWxeYiFSz6pO8a7]

---


## 🗺️ Mapa de Navegación

```
📁 Entrega 2
├── 📁 docs/
│   ├── 📄 README.md (Este archivo)
│   ├── 🎯 analisis_problema.md
│   ├── 📚 estado_arte.md
│   ├── 📅 planeacion.md
│   ├── ⚙️ Instalacion.md
│   └── 📁 otros/
│       └── 📄 Entregas.pdf
├── 📁 src/
│   ├── 📁 data/
│   │   └── 📊 preprocess.ipynb (Análisis exploratorio)
│   ├── 📁 models/
│   │   ├── 📊 1_linear_regression.ipynb
│   │   ├── 📊 2_moving_averages.ipynb
│   │   ├── 📊 3_time_series_smoothing.ipynb
│   │   ├── 📊 4_time_series_regression.ipynb
│   │   └── 📊 5_time_series_arima.ipynb
│   └── 📁 utils/
│       └── ⚙️ funcions.ipynb (Funciones reutilizables)
└── 📁 results/
```

---

*Este documento será actualizado continuamente conforme avance el proyecto y se identifiquen nuevos requerimientos o cambios en el alcance.*

---

## Extras: Iconografía

### Estados del Proyecto

| Icono | Estado | Descripción | Uso |
|-------|--------|-------------|-----|
| ⏳ | **Pendiente** | Tarea o documento por iniciar | `⏳ Pendiente` |
| 🔄 | **En Progreso** | Tarea o documento en desarrollo | `🔄 En Progreso` |
| ✅ | **Completado** | Tarea o documento finalizado | `✅ Completado` |
| ❌ | **Descartado** | Tarea o documento cancelado | `❌ Descartado` |

### Estados Alternativos

| Icono | Estado | Descripción | Uso |
|-------|--------|-------------|-----|
| 📋 | **Por Hacer** | Tarea pendiente de asignación | `📋 Por Hacer` |
| 🚧 | **En Construcción** | Desarrollo activo | `🚧 En Construcción` |
| 🎯 | **Objetivo** | Meta o objetivo específico | `🎯 Objetivo` |
| ⚠️ | **Advertencia** | Requiere atención | `⚠️ Advertencia` |
| 🔍 | **Revisión** | Necesita revisión | `🔍 Revisión` |
| 📝 | **Documentación** | En proceso de documentación | `📝 Documentación` |

### Ejemplos de Uso

```markdown
## Estado de Tareas
- ⏳ Análisis de requerimientos
- 🔄 Desarrollo de modelos
- ✅ Documentación inicial
- ❌ Prototipo descartado
```

