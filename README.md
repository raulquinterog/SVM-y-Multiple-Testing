# A3.1 – SVM y Multiple Testing

---

## Archivos de datos

- [A3.1 Khan.csv](https://github.com/raulquinterog/SVM-y-Multiple-Testing/blob/207a342eceeb7489c7d0c804e8dfbdb7571bd95e/A3.1%20Khan.csv): archivo con 83 muestras y 2309 columnas (2308 genes + clase)
- [A3.1.SVM.ipynb](https://github.com/raulquinterog/SVM-y-Multiple-Testing/blob/207a342eceeb7489c7d0c804e8dfbdb7571bd95e/A3.1.SVM.ipynb): archivo con el código

---

## Descripción general

Esta ejercicio analiza la expresión génica en una base de datos con 83 muestras y 2308 variables (genes), clasificadas en 4 tipos de cáncer. Se busca:

1. Identificar genes con diferencias significativas de expresión entre clases.
2. Aplicar métodos de corrección por múltiples pruebas.
3. Evaluar expresiones diferenciales en un contexto multiclase mediante ANOVA.
4. Entrenar y comparar modelos de SVM con diferentes kernels.

---

## Estructura de la notebook

### Paso 1: Exploración de datos
- Importación y limpieza de datos.
- Cálculo de diferencias de medias entre clases 2 y 4.
- Identificación de los 10 genes con mayor diferencia.

### Paso 2: Inferencia entre 2 clases (clase 2 vs 4)
- Aplicación de pruebas t.
- Corrección por múltiples pruebas: Bonferroni, Holm, Benjamini-Hochberg.
- Selección de genes significativamente distintos.

### Paso 3: Inferencia multiclase (clases 1, 2, 3 y 4)
- Pruebas ANOVA por gen.
- Corrección de p-values.
- Comparación de número de genes detectados por cada método.

### Paso 4: Entrenamiento de modelos SVM
- Selección de las 20 variables más significativas.
- Entrenamiento de modelos SVM con kernel lineal, polinomial (grado 3) y RBF.
- Evaluación de desempeño con `classification_report`.

### Paso 5: Comparación de modelos y conclusiones
- Análisis de métricas de desempeño.
- Reflexión sobre cuál kernel se adapta mejor al problema.

---

## Conclusiones

- Se detectaron cientos de genes con expresión diferencial entre tipos de cáncer.
- El uso de métodos de corrección afecta significativamente la cantidad de genes detectados.
- Los modelos SVM con kernel lineal y RBF ofrecieron el mejor desempeño, alcanzando precisión perfecta en el conjunto de prueba.
- La selección adecuada de características y el kernel influye de forma crítica en la calidad de los modelos.

---
