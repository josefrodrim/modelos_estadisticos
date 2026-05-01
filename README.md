# Modelos Estadisticos / Statistical Models

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-From%20Scratch-013243?logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Applied%20ML-F7931E?logo=scikitlearn&logoColor=white)
![Language](https://img.shields.io/badge/Language-Spanish%2FEnglish-555555)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Curso practico en notebooks sobre regresion, clasificacion y reduccion de dimensionalidad, con enfoque en derivaciones matematicas + implementacion aplicada.

Practical notebook-based course on regression, classification, and dimensionality reduction, combining mathematical derivations with applied implementation.

**[Espanol](#espanol) · [English](#english)**

---

<a name="espanol"></a>
## Espanol

### Que es este repositorio
- Material de curso de **Modelos Estadisticos** en formato notebook.
- Cobertura principal: **OLS, Regresion Logistica, LDA/QDA, PCA/SVD**.
- Enfoque pedagogico: primero implementacion "from scratch" con NumPy y luego uso de scikit-learn.

### Estructura
```text
modelos_estadisticos/
|- Clase_1 ... Clase_11/   # contenido por clase
|  |- Notebook(s)/         # notebooks teoricos y ejercicios
|  `- PPT(s)/              # diapositivas de apoyo
`- Tarea_2/                # proyectos aplicados (credit risk + PCA)
```

### Ruta sugerida
1. **Clase_1 -> Clase_4**: fundamentos de regresion lineal e inferencia.
2. **Clase_5 -> Clase_7**: regresion logistica, evaluacion y threshold.
3. **Clase_8 -> Clase_9**: LDA/QDA y clasificacion.
4. **Clase_10 -> Clase_11**: PCA, SVD e interpretacion.
5. **Tarea_2/**: integracion aplicada (riesgo crediticio y reduccion de variables).

### Notebooks clave
- `Clase_1/Notebook /Clase01_Algebra_Lineal_Final.ipynb`
- `Clase_5/Notebooks/Clase05_RegresionLogistica.ipynb`
- `Clase_7/Notebooks/Clase07_Scoring_Threshold_CreditRisk.ipynb`
- `Clase_10/Notebooks/Clase10_PCA_SVD.ipynb`
- `Tarea_2/Clase07_Scoring_Threshold_CreditRisk.ipynb`
- `Tarea_2/PCA_CreditRisk.ipynb`

### Setup rapido
```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install jupyter numpy pandas scikit-learn scipy matplotlib
jupyter notebook
```

### Notas importantes
- Notebooks principalmente en espanol (comentarios mixtos espanol/ingles).
- Reproducibilidad usual con `np.random.seed(42)`.
- En `Tarea_2/`, la variable objetivo es `default_in_last_6months`.

### Licencia
Este proyecto esta bajo la licencia MIT. Ver `LICENSE`.

---

<a name="english"></a>
## English

### What this repository is
- A **Statistical Models** course repository built around notebooks.
- Main topics: **OLS, Logistic Regression, LDA/QDA, PCA/SVD**.
- Teaching style: "from scratch" NumPy derivations first, then scikit-learn implementations.

### Repository layout
```text
modelos_estadisticos/
|- Clase_1 ... Clase_11/   # class-by-class content
|  |- Notebook(s)/         # theory and exercise notebooks
|  `- PPT(s)/              # supporting slides
`- Tarea_2/                # applied projects (credit risk + PCA)
```

### Suggested learning flow
1. **Clase_1 -> Clase_4**: linear regression and inference foundations.
2. **Clase_5 -> Clase_7**: logistic regression, evaluation, and threshold selection.
3. **Clase_8 -> Clase_9**: LDA/QDA and discriminant classification.
4. **Clase_10 -> Clase_11**: PCA, SVD, and interpretation.
5. **Tarea_2/**: applied integration on credit-risk datasets.

### Key notebooks
- `Clase_1/Notebook /Clase01_Algebra_Lineal_Final.ipynb`
- `Clase_5/Notebooks/Clase05_RegresionLogistica.ipynb`
- `Clase_7/Notebooks/Clase07_Scoring_Threshold_CreditRisk.ipynb`
- `Clase_10/Notebooks/Clase10_PCA_SVD.ipynb`
- `Tarea_2/Clase07_Scoring_Threshold_CreditRisk.ipynb`
- `Tarea_2/PCA_CreditRisk.ipynb`

### Quick setup
```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install jupyter numpy pandas scikit-learn scipy matplotlib
jupyter notebook
```

### Important notes
- Most notebooks are in Spanish (code comments are mixed Spanish/English).
- Reproducibility is usually set with `np.random.seed(42)`.
- In `Tarea_2/`, the binary target is `default_in_last_6months`.

### License
This project is licensed under the MIT License. See `LICENSE`.
