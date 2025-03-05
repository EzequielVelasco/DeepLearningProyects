# DeepLearningProyects
Este repositorio documenta la evolución de diferentes modelos de redes neuronales aplicadas a visión por computadora, con un enfoque en la mejora del desempeño y la reducción del overfitting.

Modelos desarrollados

## 1° Modelo

Se agregaron dos capas convolucionales adicionales (64 y 128 filtros).

Implementación de EarlyStopping para evitar overfitting.

Aumento del número de épocas a 200.

Resultado: AUC de 73.3%, pero con alto overfitting.

## 2° Modelo

Se incorporaron tres capas de dropout.

Resultado: AUC mejorado a 77.43%, con menor overfitting.

## 3° Modelo

Se duplicaron las capas convolucionales antes de cada capa de pooling.

Se añadieron BatchNormalization para estabilizar el entrenamiento.

Resultado: AUC de 80.36%, aunque persiste el overfitting.

## 4° Modelo

Aumento del batch_size de 64 a 128.

Profundización de capas convolucionales (64→128→256 filtros).

Mayor uso de dropout para mitigar el overfitting.

Resultado: Mejora en el desempeño, red más compleja.

## 5° Modelo

Se agregaron kernel_regularizer y kernel_initializer.

Cambio del optimizador Adam a SGD.

Resultado: Menor overfitting, mayor estabilidad en la convergencia.

## 6° Modelo

Reducción de la regularización kernel_regularizer.

Incremento en la cantidad de parámetros y capas densas.

Resultado: Pequeñas diferencias en accuracy, pero mejor generalización del modelo anterior.

## 7° Modelo

Eliminación de kernel_regularizer y kernel_initializer.

Alternancia de funciones de activación (ReLU y Swish).

Se aumentó la patience de los callbacks.

Se añadió una capa convolucional de 512 filtros.

Resultado: Accuracy de 88.56%, con correcta convergencia de train y test.

## 8° Modelo

Introducción de data augmentation (desplazamientos, rotación, espejado, etc.).

Red neuronal más sencilla con menos parámetros.

Resultado: Accuracy de 88%, con menor overfitting.

## 9° Modelo

Alternancia de funciones de activación (Swish y ReLU).

Capa adicional de 512 filtros.

Uso de data augmentation.

Resultado: Accuracy de 90.45%, con una red más eficiente.

## 10° Modelo (Modelo Ganador)

Pares de capas convolucionales de 128, 256, 512 y 1024 filtros.

Capas densas finales de 1024 neuronas.

Data augmentation mejorado con variación de zoom del 20%.

Resultado: AUC de 91.35%, con una red más compleja (37M de parámetros).

# Conclusión

El modelo final alcanza el mejor desempeño, pero su alto costo computacional plantea la pregunta sobre si realmente es la mejor opción en términos de eficiencia. Se pueden evaluar métodos alternativos como reducción de parámetros o modelos preentrenados para balancear precisión y costo de cómputo.
