# Intrusion Detection System (IDS) con Deep Learning y XAI

Este repositorio contiene la implementación y reproducción experimental de un Sistema de Detección de Intrusiones (IDS) basado en Inteligencia Artificial, evaluado sobre el dataset de llamadas al sistema **ADFA-LD**. 

El proyecto no solo se enfoca en crear un modelo de alta precisión ("Caja Negra"), sino en auditar sus decisiones utilizando técnicas de **Inteligencia Artificial Explicable (XAI)** y comprobando su robustez mediante Análisis de Perturbación.

## Características Principales

* **Arquitectura Deep Learning:** Implementación de un Perceptrón Multicapa (MLP) de 4 capas optimizado para clasificación binaria de secuencias (*n-grams*).
* **Alta Precisión:** El modelo alcanza un **96% de Accuracy** en la detección de intrusiones, superando métricas de implementaciones base.
* **Explicabilidad Local (LIME):** Extracción de Indicadores de Compromiso (IoCs) a nivel de instancia individual.
* **Explicabilidad Global (SHAP):** Uso de `KernelExplainer` para identificar las firmas de malware generales aprendidas por el firewall inteligente.
* **Análisis de Perturbación Agresiva:** Un experimento masivo automatizado que simula evasión alterando las características clave detectadas por XAI (Out-of-Distribution), validando la veracidad de las explicaciones.

## Tecnologías y Requisitos

Este proyecto fue desarrollado en **Python 3.13+**. Las dependencias principales incluyen:
* `tensorflow` / `keras` (Construcción y entrenamiento del MLP)
* `scikit-learn` (Preprocesamiento y métricas)
* `pandas` & `numpy` (Manipulación de datos)
* `lime` & `shap` (Frameworks de explicabilidad)
* `matplotlib` & `seaborn` (Visualización de datos)

## Estructura del Proyecto

* `Laboratorio.ipynb`: Jupyter Notebook principal que contiene todo el flujo de trabajo (Preprocesamiento, Entrenamiento, XAI y Perturbación).
* `adfa_ld_binary.csv`: Dataset preprocesado con extracción de *n-grams*.
* `requirements.txt`: Lista de dependencias del entorno virtual (recomendado generar uno).

