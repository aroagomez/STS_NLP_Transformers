# Similitud Textual Semantica (STS) con Transformers

Este proyecto aborda la tarea de Similitud Textual Semántica (STS) dentro del campo del Procesamiento del Lenguaje Natural (PLN). El objetivo es medir el grado de equivalencia de significado entre dos fragmentos de texto, superando las limitaciones de la simple superposición léxica mediante el uso de embeddings contextuales.

## Fases del Proyecto y Metodologia
El experimento se ha estructurado en tres fases analíticas para evaluar el rendimiento de distintas arquitecturas:

1. **Modelos Base (Baselines) No Supervisados:** Establecimiento de métricas de referencia utilizando enfoques tradicionales y modelos pre-entrenados sin ajuste específico para la tarea.
2. **Fine-Tuning Supervisado:** Ajuste fino de modelos basados en la arquitectura Transformer (BERT) utilizando datasets específicos de STS para adaptar los pesos de la red a la tarea de medición de similitud.
3. **Transferencia de Conocimiento (Cross-Lingual):** Evaluación de la capacidad de los modelos para generalizar el conocimiento semántico entre distintos idiomas (del inglés al castellano) mediante un enfoque zero-shot.

## Tecnologias Utilizadas
* **Lenguaje:** Python (Jupyter Notebooks).
* **Frameworks de PLN:** Hugging Face (transformers, datasets), sentence-transformers.
* **Modelos Evaluados:** BERT (monolingüe) y xmlROBERTa (multilingüe).

## Conclusiones Destacadas
El análisis comparativo demostró la importancia crítica de la selección del modelo base según el dominio lingüístico. 

Mientras que la arquitectura BERT estándar (entrenada predominantemente en inglés) arrojó resultados deficientes al evaluar textos en castellano, el uso de modelos multilingües como **xmlROBERTa** permitió una transferencia de conocimiento altamente efectiva. Este último fue capaz de ofrecer métricas de similitud precisas en español a pesar de haber sido ajustado (fine-tuned) de manera exclusiva con conjuntos de datos en inglés.

## Estructura del Repositorio
* `Proyecto_STS.ipynb`: Notebook principal con la carga de datasets (STS-B), importación de modelos de Hugging Face, entrenamiento (fine-tuning) y evaluación.
* `Proyecto_PLN_STS.pdf`: Memoria técnica detallada con la fundamentación teórica, estado del arte y análisis profundo de los resultados.