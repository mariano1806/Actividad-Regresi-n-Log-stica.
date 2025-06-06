# Proyecto de Regresión Logística - Predicción de Enfermedad Cardíaca

Este proyecto utiliza un modelo de **regresión logística** para predecir si una persona tiene enfermedad cardíaca a partir de variables clínicas. Está hecho en Python usando `pandas`, `scikit-learn`,`matplotlib` y 'joblib'.
---

## Estructura del Proyecto

- `Regresion_Logistica.ipynb`: Notebook con todo el análisis, entrenamiento del modelo y predicciones.
- `modelo_regresion_logistica.pkl`: Archivo guardado del modelo entrenado.
- `columnas_entrenamiento.pkl`: Lista de columnas del conjunto de entrenamiento (tras aplicar `get_dummies`).
- `env/`: Entorno virtual con las dependencias necesarias.

---

## ⚙️ Pasos del Análisis

1. **Carga y limpieza de datos**: Se eliminan columnas innecesarias como `id` y se convierte la variable objetivo `num` a binaria (`0` = sano, `1` = enfermedad).
2. **Codificación de variables categóricas**: Se aplica `pd.get_dummies()` con `drop_first=True`.
3. **División de datos**: Con `train_test_split()`.
4. **Entrenamiento del modelo**: Usando `LogisticRegression()` de `scikit-learn`.
5. **Evaluación**: Se calculan métricas de precisión y matriz de confusión.
6. **Predicción con nuevos datos**: Se arma un `DataFrame` con los datos de un paciente y se aplica el mismo preprocesamiento para predecir con el modelo entrenado.

✅ Resultado esperado
El modelo devuelve si un nuevo paciente tiene (1) o no tiene (0) enfermedad cardíaca, basado en sus datos clínicos.
