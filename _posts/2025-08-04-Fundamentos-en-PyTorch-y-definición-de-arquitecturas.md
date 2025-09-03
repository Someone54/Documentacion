---
title: Fundamentos en PyTorch y definición de arquitecturas
tags: Acta
---

## Discusión
En la sesión se revisaron los videos de la playlist asignada sobre fundamentos de redes neuronales en PyTorch, comentando que estos materiales han permitido a los integrantes familiarizarse con los conceptos básicos y que servirán como base para el desarrollo del proyecto, particularmente en lo relacionado con el cálculo de macropropiedades de materiales arquitectados. Se reiteró el objetivo central del trabajo, consistente en diseñar una red neuronal capaz de predecir propiedades mecánicas, como el módulo de Young y el coeficiente de Poisson, a partir del análisis microestructural de materiales arquitectados. Como caso de estudio se definió trabajar con tejido óseo, considerando tanto el hueso compacto (cortical) como el hueso esponjoso (trabecular), en el marco de la colaboración con una universidad en Chile que podrá suministrar datos experimentales para validar el modelo. Asimismo, se discutió la importancia de estructurar las arquitecturas de la red neuronal con base en el paper de referencia, estableciendo que cada grupo de trabajo desarrollará un conjunto de modelos variando parámetros como el tamaño de los filtros y el número de capas, además de incorporar modificaciones adicionales que permitan explorar el comportamiento de la red en diferentes configuraciones. Finalmente, se resaltó que, en esta etapa inicial, se emplearán los datos de los videos únicamente para verificar el correcto funcionamiento del código, y que posteriormente, cuando los datos reales estén disponibles, podrán integrarse directamente en el modelo para su validación.


## Tareas asignadas
- **Investigación de propiedades mecánicas del hueso compacto y esponjoso**  
  Esta actividad quedó pendiente para la próxima reunión, con el fin de recopilar información de referencia que permita orientar el entrenamiento y validación de la red neuronal.  

- **Definición de arquitecturas de red neuronal**  
  Cada grupo debe proponer un total de **5 arquitecturas de red neuronal**.  
  - **2 arquitecturas base:** variaciones estrictas de la referencia del paper, modificando únicamente:  
    - Tamaño del filtro (kernel).  
    - Tamaño de las capas (salidas de la convolucional o fully connected layer).  
  - **3 arquitecturas adicionales:** modificaciones más amplias, tales como:  
    - Añadir capas ocultas.  
    - Aumentar el número de capas por una razón justificada.  
    - Variar parámetros adicionales, siempre garantizando compatibilidad.
