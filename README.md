# Datathon2024_AtleticoDelIIMAS

# InterConNet: Sistema de Análisis de Contrataciones y Conflictos de Interés

## Descripción

**InterConNet** es una plataforma diseñada para detectar conflictos de interés y patrones de corrupción en procesos de contratación. Utiliza análisis de redes y algoritmos de machine learning para identificar conexiones ocultas entre contratantes y empleados, enfocándose en posibles relaciones de sanciones y conflictos de interés.

## Funcionalidades

1. **Carga de Datos**: Permite cargar archivos que contienen información sobre contratantes y empleados.
2. **Análisis de Redes**: Genera un grafo que representa las relaciones entre contratantes y empleados, permitiendo identificar vecindades y comunidades. Esto ayuda a detectar posibles conflictos de interés y conexiones con empleados sancionados.
3. **Machine Learning**: Utiliza representaciones vectoriales generadas a partir del grafo para aplicar algoritmos de machine learning y deep learning, buscando patrones de corrupción y anomalías en los datos.
4. **Matriz de Confusión**: Visualiza el rendimiento del modelo mediante una matriz de confusión, comparando las predicciones con los resultados reales.

## Tecnologías Utilizadas

- **Python**: Lenguaje de programación principal.
- **Matplotlib**: Para la visualización de la matriz de confusión.
- **Seaborn**: Para mejorar la presentación visual de las matrices.
- **Scikit-learn**: Para la creación de la matriz de confusión y la implementación de modelos de machine learning.


### Detalles de implementación

Los modelos entrenados fueron usando los datos de michoacán debido a la cantidad límitada de información que teníamos para los demás estados:

1. **NetworkX**: creación de grafo dirigido y su respectivo análisis.
2. **Node2Vec**: creación de embedding de las relaciones entre nodos.
3. **Regresión Logística**: modelo entrenado para responder ¿el funcionario puede recibir sanciones?
4. **Clustering jerarquico**: encontrar una jerarquía entre las relaciones existentes, se esperan dos clusters siendo uno con funcionarios sancionados y no sancionados.
5. **Clustering DSBCAN**: clustering para encontrar anomalías

### Trabajo en el futuro

1. Modelo de aprendizaje supervisado para multiclasificación de las diferentes tipos de faltas que puede distinguirse de un funcionario.
