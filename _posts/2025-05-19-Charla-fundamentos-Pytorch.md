---
title: Acta charla fundamentos de Pytorch
tags: Charla
---

## Fundamentos básicos del uso de Pytorch para la creación de redes neuronales

Durante la sesión del semillero se abordaron conceptos fundamentales sobre redes neuronales y su implementación práctica utilizando PyTorch. Se explicó la arquitectura general de una red neuronal, partiendo desde una capa de entrada que recibe los datos en forma matricial o vectorial, pasando por varias capas ocultas encargadas de procesar y transformar la información mediante funciones de activación y operaciones de aprendizaje, hasta llegar a una capa de salida que entrega una predicción o resultado final. En este proceso también se hizo mención al uso de embeddings como técnica para representar características complejas de los datos de manera más eficiente.
Además, se discutió la estructura típica de un proyecto de machine learning, dividiendo los datos en tres subconjuntos: entrenamiento, validación y prueba. Se hizo énfasis en la importancia de normalizar los datos antes de ser introducidos al modelo, así como en la evaluación del desempeño mediante métricas que comparan las predicciones del modelo con los valores reales (ground truth). Durante la explicación se utilizó un ejemplo gráfico de regresión lineal, representado por la ecuación $y = mx + b$, para ilustrar conceptos básicos del aprendizaje supervisado.

También se mencionaron herramientas del entorno PyTorch como los datasets, dataloaders y algunas utilidades adicionales que facilitan el manejo de los datos y la estructura modular del modelo. Todo esto indica que el proyecto en el que se está trabajando probablemente involucra el entrenamiento de modelos predictivos o de clasificación, basados en datos previamente recolectados y organizados, con el objetivo de aplicar técnicas de inteligencia artificial dentro de un marco experimental o aplicado.

**Entrada (Input):** Se representa con una figura que podría ser una matriz o un vector (posiblemente imágenes o datos tabulares).
Procesamiento: Varias capas ocultas interconectadas que transforman progresivamente los datos (hay menciones a embedding, lo que indica codificación de características).

**Salida (Output)**: Resultado del modelo, se menciona algo como "función de costo" y "función de activación".

**Linealidad:** Se introduce el modelo lineal  𝑦 = 𝑚𝑥 + 𝑏, indicando que se habló también de regresión lineal básica.

El proceso de funcionamiento de pytorch se podría resumir de la siguiente manera:
1. **Datos y Preprocesamiento:** El primer paso es tener los datos. Estos datos se dividen típicamente en tres conjuntos:
-	Train (Entrenamiento): El conjunto de datos que se usa para que el modelo aprenda.
-	Val (Validación): Se utiliza durante el entrenamiento para evaluar el rendimiento del modelo en datos que no ha visto.
-	Test (Prueba): Se usa al final, después de que el modelo ha sido entrenado, para dar una evaluación final del rendimiento del modelo.
Antes de usarlos, los datos se normalizan y se preparan. PyTorch tiene una clase llamada Dataset y Dataloader para manejar los datos, facilitando su carga y la creación de lotes (batches) para el entrenamiento.
2. **Creación del Modelo de Red Neuronal:** Una red neuronal, como se ve en las imágenes, se compone de múltiples capas. La imagen muestra un ejemplo de una red neuronal, donde la entrada (Input) pasa por una serie de capas de procesamiento (Pross. Cractet) y finalmente produce una salida (Output). En PyTorch, se usa la clase nn.Module para construir la arquitectura de la red.

3. **Entrenamiento y Métricas:** Una vez que el modelo está definido, el entrenamiento consiste en los siguientes pasos, que se repiten en un ciclo:
-	Predicción: El modelo toma los datos de entrada y produce una predicción.
-	Cálculo de la función de costo: Se compara la predicción del modelo con la etiqueta real (GT o True) usando una función de costo (o loss function). Esto nos dice qué tan bien está el modelo.
-	Backpropagation: El error se propaga hacia atrás a través de la red para ajustar los pesos del modelo. Esta es la parte donde el modelo realmente aprende.

**Actualización de los pesos:** Se usan optimizadores (como SGD, Adam, etc.) para ajustar los pesos del modelo y reducir el error. En cada paso, se evalúan métricas para medir el rendimiento del modelo, como la precisión (accuracy), la pérdida (loss), etc.