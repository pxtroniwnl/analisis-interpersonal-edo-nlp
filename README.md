# Dinámica de Relaciones: Aplicación del Modelo de Gottman-Murray mediante EDO

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![NLP](https://img.shields.io/badge/NLP-Sentiment%20Analysis-green.svg)
![UTB](https://img.shields.io/badge/Institución-UTB-orange.svg)

## 📌 Descripción del Proyecto
Este proyecto implementa el **Modelo de Gottman-Murray**, un sistema de **Ecuaciones Diferenciales Ordinarias (EDO) acopladas**, para analizar y predecir la evolución del afecto en interacciones interpersonales. Utilizando el **Cornell Movie-Dialogs Corpus**, transformamos diálogos de ficción en series de tiempo numéricas para identificar patrones de estabilidad y conflicto.

## 🚀 Objetivos Técnicos
* [cite_start]**Inferencia de Parámetros:** Estimar niveles de inercia emocional ($r$) e influencia mutua ($I$) mediante algoritmos de optimización. [cite: 1]
* [cite_start]**Análisis de Estabilidad:** Localizar atractores y puntos de equilibrio emocionales para predecir el desenlace de una interacción. [cite: 1]
* [cite_start]**Validación:** Comparar la trayectoria teórica del modelo con la evolución real de los sentimientos extraídos del texto. [cite: 1]

## 📊 Fundamentos Matemáticos
El núcleo del análisis se basa en el siguiente sistema diferencial, donde el cambio emocional de una persona depende de su estado previo y de la influencia de su interlocutor:

$$\frac{dW}{dt} = a + r_w W(t) + I_{hw}(H(t))$$
$$\frac{dH}{dt} = b + r_h H(t) + I_{wh}(W(t))$$

Donde:
* [cite_start]**$a, b$:** Estado base emocional (humor natural). [cite: 1]
* [cite_start]**$r_w, r_h$:** Inercia emocional (resistencia al cambio de humor). [cite: 1]
* [cite_start]**$I_{hw}, I_{wh}$:** Funciones de influencia (acoplamiento del sistema). [cite: 1]

## 🛠️ Pipeline de Ejecución
1. [cite_start]**ETL:** Limpieza y estructuración del Cornell Movie-Dialogs Corpus para identificar parejas de personajes con interacciones significativas. [cite: 1]
2. [cite_start]**Sentiment Analysis:** Procesamiento de lenguaje natural (NLP) para asignar puntajes de afecto a cada turno de palabra. [cite: 1]
3. [cite_start]**Optimización:** Uso de `scipy.optimize` para ajustar los parámetros de la EDO a los datos reales. [cite: 1]
4. [cite_start]**Simulación:** Resolución numérica para proyectar si la relación converge a un estado estable positivo o negativo. [cite: 1]

## 🏢 Impacto en Clima Organizacional
Más allá del análisis cinematográfico, este modelo es aplicable en **People Analytics** para:
* [cite_start]**Predecir el Burnout:** Detectar equipos cuya inercia emocional se vuelve irreversiblemente negativa. [cite: 1]
* [cite_start]**Optimizar el Liderazgo:** Evaluar cómo la influencia de un líder afecta la respuesta emocional y productividad de su grupo. [cite: 1]
* [cite_start]**Retención de Talento:** Identificar dinámicas de equipo que tienden a puntos de equilibrio de ruptura. [cite: 1]

---
**Autor:** Alejandro Patrón Montero  
**Facultad:** Ingeniería - Ciencia de Datos  
**Institución:** Universidad Tecnológica de Bolívar (Cartagena, Colombia)
