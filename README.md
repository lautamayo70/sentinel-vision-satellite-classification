## 🛰️ Sobre el Proyecto
Sentinel-Vision es un sistema de visión artificial diseñado para la clasificación multiclase de imágenes satelitales utilizando el dataset **EuroSAT**. Este proyecto implementa técnicas de **Deep Learning** y **Computer Vision** para identificar diferentes tipos de uso de suelo (bosques, carreteras, zonas industriales, etc.).

El proyecto fue desarrollado como parte de un flujo de trabajo de **MLOps**, integrando almacenamiento en la nube y procesamiento distribuido.

## 🛠️ Tecnologías y Herramientas
*   **Lenguaje:** Python 3.12
*   **Framework:** TensorFlow / Keras (Functional API)
*   **Modelo Base:** MobileNetV2 (Transfer Learning con pesos de ImageNet)
*   **Infraestructura:** Google Cloud Platform (Vertex AI & Cloud Storage)
*   **Aceleración:** NVIDIA T4 GPU (Google Colab)

## 🏗️ Arquitectura del Pipeline
Una de las fortalezas de este proyecto es la optimización del flujo de datos:
- **Almacenamiento:** Los datos se consumen directamente desde un Bucket de **Google Cloud Storage**.
- **Eficiencia:** Implementación de la API `tf.data` con técnicas de `prefetch` y `parallel_calls` para mitigar cuellos de botella de I/O entre el almacenamiento en la nube y el entrenamiento en GPU.
- **Modelado:** Arquitectura basada en Transfer Learning para maximizar la precisión en un entorno de recursos computacionales eficientes.

## 📂 Estructura del Repositorio
- `notebooks/`: Contiene la experimentación inicial en Vertex AI y el entrenamiento final optimizado en Google Colab.
- `assets/`: Diagramas de arquitectura y despliegue.

## 🚀 Próximos Pasos (Roadmap)
- [ ] Exportación del modelo a formato SavedModel.
- [ ] Despliegue de un Endpoint en Vertex AI para inferencia en tiempo real.
- [ ] Integración con un dashboard en Power BI para visualización de métricas geoespaciales.

---
Desarrollado por **Laura Tamayo Cardona** 🇨🇴 - Ingeniera Informática de la Institución Universitaria de Envigado.
