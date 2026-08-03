# 📞 Análisis de Clientes y Segmentación — ConnectaTel

Este proyecto realiza un análisis exploratorio de datos (EDA), limpieza, segmentación y detección de patrones de consumo para la empresa de telecomunicaciones **ConnectaTel**. El objetivo principal es comprender el comportamiento de uso de los clientes según su plan y grupo demográfico para generar recomendaciones accionables de negocio.

---

## 🎯 Objetivos del Proyecto
* **Limpieza e Integridad de Datos:** Tratar valores ausentes (`NaN`) sin sesgar la base de datos de usuarios.
* **Análisis Exploratorio y Outliers:** Identificar distribuciones de edad, llamadas y mensajes, evaluando valores atípicos mediante el método de Rango Intercuartílico (IQR).
* **Segmentación de Clientes:** Clasificar a la base de usuarios según su edad (`grupo_edad`) y nivel de tráfico (`grupo_uso`).
* **Insights Ejecutivos:** Traducir hallazgos técnicos en decisiones comerciales para la retención y migración (*up-selling*) de clientes.

---

## 📁 Datasets Utilizados
El análisis combina dos fuentes principales de datos:
1. `users`: Información demográfica de los clientes (ID, edad, tipo de plan asignado).
2. `usage`: Historial de tráfico y consumo registrado (cantidad de llamadas, cantidad de mensajes y total de minutos consumidos).

---

## ⚙️ Etapas del Análisis
1. **Carga e Inspección Inicial:** Verificación de tipos de datos y estructuras.
2. **Tratamiento de Datos Nulos:** Imputación estratégica con `0` (`.fillna(0)`) para usuarios sin actividad registrada, preservando el 100% de la muestra.
3. **Análisis Visual de Distribuciones:** Generación de histogramas para evaluar el comportamiento de variables clave por plan.
4. **Evaluación de Outliers:** Construcción de boxplots en bucle `for` y cálculo de límites IQR superiores.
5. **Segmentación Multidimensional:**
   * **Por Uso:** Categorización en *Bajo uso*, *Uso medio* y *Alto uso* con `np.select()`.
   * **Por Edad:** Clasificación en *Joven* (<30), *Adulto* (30-59) y *Adulto Mayor* (60+).
6. **Conclusiones Ejecutivas:** Elaboración de un resumen estratégico para los stakeholders del proyecto.

---

## 🚀 Cómo Ejecutar el Notebook

### Opción 1: Google Colab (Recomendado)
1. Haz clic en el siguiente enlace o abre Google Colab.
2. Ve a **Archivo** ➔ **Abrir cuaderno** ➔ Pestaña **GitHub**.
3. Pastea la URL de este repositorio y selecciona el archivo `.ipynb`.
4. https://colab.research.google.com/drive/1Seek51lYV4Dtz6xjlrRoGIjHikp9V_10?usp=sharing
