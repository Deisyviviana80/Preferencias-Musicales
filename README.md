# 🎵 Análisis de Preferencias Musicales - Springfield vs Shelbyville

## 📌 Descripción

Proyecto de análisis de datos desarrollado como parte del bootcamp de **Analista de Datos en TripleTen**.

El objetivo es comparar el comportamiento musical de usuarios de dos ciudades — **Springfield** y **Shelbyville** — y determinar si la actividad difiere según el día de la semana. Para lograrlo se aplicó un flujo completo de análisis: exploración, limpieza de datos y prueba de hipótesis.

---

## 🔬 Hipótesis

> *"La actividad de los usuarios difiere según el día de la semana y dependiendo de la ciudad."*

---

## 📁 Estructura del proyecto

```
├── musica_analisis_limpio.ipynb   # Notebook principal con el análisis completo
├── music_project_en.csv           # Dataset de reproducciones musicales
└── README.md
```

---

## 🔄 Flujo de análisis

### 1. 🔍 Descripción de los datos
- Carga e inspección inicial del dataset (65.079 registros, 7 columnas)
- Identificación de tipos de datos, columnas y posibles problemas de calidad

### 2. 🧹 Preprocesamiento
- **Estandarización de encabezados:** minúsculas, eliminación de espacios, snake_case
- **Valores ausentes:** 10.108 valores nulos en `track`, `artist` y `genre` → reemplazados por `'unknown'`
- **Duplicados explícitos:** se identificaron y eliminaron 3.826 filas duplicadas
- **Duplicados implícitos:** corrección de variantes del género `hiphop` (`hip`, `hop`, `hip-hop`)

### 3. 📊 Prueba de hipótesis
Comparación de reproducciones por ciudad y día de la semana (lunes, miércoles y viernes):

| Ciudad       | Lunes  | Miércoles | Viernes |
|-------------|--------|-----------|---------|
| Springfield  | 15.740 | 11.056    | 15.945  |
| Shelbyville  | 5.614  | 7.003     | 5.895   |

**🔎 Hallazgos:**
- En **Springfield**, la actividad es alta y relativamente estable el lunes y viernes, con una caída notable el miércoles.
- En **Shelbyville**, el patrón es diferente: el miércoles es el día con mayor actividad relativa.
- ✅ La hipótesis **se confirma**: el comportamiento sí varía según ciudad y día de la semana.

---

## 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

- 🐍 **Python 3**
- 🐼 **Pandas** — manipulación y análisis de datos
- 📓 **Jupyter Notebook** — entorno de desarrollo

---

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Deisyviviana80/Preferencias-Musicales
   ```

2. Instala las dependencias:
   ```bash
   pip install pandas jupyter
   ```

3. Abre el notebook:
   ```bash
   jupyter notebook musica_analisis_limpio.ipynb
   ```

> ⚠️ Asegúrate de que el archivo `music_project_en.csv` esté en el mismo directorio que el notebook.

---

## 💭 Reflexiones finales

Este proyecto me permitió aplicar por primera vez un flujo completo de análisis de datos sobre un dataset real: desde entender qué hay en los datos, pasando por limpiarlos, hasta llegar a una conclusión basada en evidencia.

Uno de los aprendizajes más importantes fue que los datos rara vez vienen listos para analizar — el preprocesamiento no es un paso menor, sino una parte esencial del trabajo. También aprendí que una hipótesis no siempre se confirma o rechaza de forma tajante: a veces los datos nos invitan a hacer más preguntas y a buscar más información antes de tomar decisiones.

Como mejora futura, sería valioso incorporar datos de más ciudades y más días de la semana, y aplicar pruebas estadísticas formales para dar mayor solidez a las conclusiones.

---

## 👤 Autor

**Deisy Viviana Hurtado Vega**  
Practica de Análisis de Datos — TripleTen
