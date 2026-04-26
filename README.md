# Modelos Estadísticos / Statistical Models

**[Español](#español) · [English](#english)**

---

<a name="español"></a>
# Español

Repositorio del curso de **Modelos Estadísticos**, que cubre regresión lineal, regresión logística, análisis discriminante y reducción de dimensionalidad. Cada clase incluye un notebook teórico con derivaciones matemáticas paso a paso y un notebook de ejercicios con dificultad progresiva.

## Estructura del repositorio

```
modelos_estadisticos/
├── Clase_1/          # Álgebra lineal y mínimos cuadrados
├── Clase_2/          # Eigendescomposición y distribución de β̂
├── Clase_3/          # Supuestos Gauss-Markov y BLUE
├── Clase_4/          # Inferencia: R², ANOVA, t-tests
├── Clase_5/          # Regresión logística y MLE
├── Clase_6/          # Evaluación y diagnósticos del modelo logístico
├── Clase_7/          # Threshold óptimo y scoring crediticio
├── Clase_8/          # Análisis Discriminante Lineal (LDA)
├── Clase_9/          # QDA y segmentación de clientes
├── Clase_10/         # PCA y SVD
├── Clase_11/         # Criterios de selección e interpretación PCA
└── Tarea_2/          # Proyectos aplicados: credit risk + PCA
```

## Módulos

### Módulo 1 — Regresión Lineal (Clases 1–4)

Fundamentos de OLS desde álgebra matricial hasta inferencia estadística completa.

| Clase | Tema | Conceptos clave |
|-------|------|-----------------|
| **1** | Álgebra lineal y OLS | Ecuaciones normales XᵀX β = Xᵀy, matriz sombrero H, condición de rango |
| **2** | Eigendescomposición y distribución de β̂ | Eigenvalores de XᵀX, distribución normal multivariada, varianza de β̂ |
| **3** | Gauss-Markov y BLUE | 5 supuestos, insesgadez, homocedasticidad, diagnósticos de residuos |
| **4** | Inferencia y reporte | R², tabla ANOVA, prueba F, pruebas t, intervalos de confianza |

**Datasets:** California Housing, predicción de salarios.

**Funciones construidas desde cero:** `ols_fit()`, `ols_summary()`, `ols_diagnostics()`, `describe_sigma()`

---

### Módulo 2 — Regresión Logística (Clases 5–7)

Clasificación binaria mediante el modelo lineal generalizado.

| Clase | Tema | Conceptos clave |
|-------|------|-----------------|
| **5** | GLM y función logit | Por qué OLS falla en {0,1}, función sigmoide σ(z), MLE, gradient descent |
| **6** | Evaluación y diagnósticos | Devianza vs SSE, AIC, prueba de Wald (z-stats), Pseudo R² McFadden, ROC/AUC |
| **7** | Threshold y scoring | Selección de umbral basada en costos, Logística vs LDA, pipeline de crédito |

**Datasets:** Detección de fraude bancario, default crediticio.

---

### Módulo 3 — Análisis Discriminante (Clases 8–9)

Clasificación mediante maximización de varianza entre clases.

| Clase | Tema | Conceptos clave |
|-------|------|-----------------|
| **8** | LDA y criterio de Fisher | Matrices Sᵦ y Sᵥᵥ, fronteras lineales, reducción multiclase |
| **9** | QDA y aplicaciones | Fronteras cuadráticas cuando Σₖ difiere, matriz de confusión por clase |

**Datasets:** Segmentación de clientes (Familiar / Joven Urbano / Senior).

---

### Módulo 4 — Análisis de Componentes Principales (Clases 10–11)

Reducción de dimensionalidad no supervisada por maximización de varianza.

| Clase | Tema | Conceptos clave |
|-------|------|-----------------|
| **10** | PCA y SVD | Eigendescomposición de la covarianza, equivalencia con SVD, scree plot, biplot |
| **11** | Selección e interpretación | Criterios: % varianza, Kaiser, codo; loadings; error de reconstrucción; pipeline |

**Datasets:** Datos financieros con 8 variables correlacionadas (ingresos, deuda, mora_30d, mora_90d, etc.)

---

### Tarea 2 — Proyectos aplicados

| Notebook | Descripción |
|----------|-------------|
| `Clase07_Scoring_Threshold_CreditRisk.ipynb` | Pipeline completo de scoring crediticio con optimización de umbral por costo |
| `PCA_CreditRisk.ipynb` | PCA aplicado a datos de crédito para reducción de features antes de clasificación |

---

## Estructura de cada clase

Cada clase contiene dos notebooks:

**Notebook principal** (`ClaseXX_Tema.ipynb`)
- Derivaciones matemáticas completas (no solo fórmulas)
- Implementación desde cero con NumPy antes de usar scikit-learn
- Dataset real con interpretación en contexto de negocio
- Visualizaciones con propósito pedagógico (curvas ROC, scree plots, biplots, superficies 3D)

**Notebook de ejercicios** (`ClaseXX_Ejercicios.ipynb`)
- Dificultad progresiva: 🟢 básico · 🟡 intermedio · 🔴 avanzado
- Estructura: enunciado → tu código → solución de referencia
- Los ejercicios se encadenan; la solución de uno es insumo del siguiente

---

## Stack tecnológico

| Librería | Uso |
|----------|-----|
| Python 3.11 | Lenguaje base |
| NumPy | Álgebra lineal y cálculo matricial |
| Pandas | Manipulación de datos tabulares |
| scikit-learn | Modelos de producción y evaluación |
| SciPy | Distribuciones estadísticas (t, F, χ²) |
| Matplotlib | Visualizaciones |

---

## Instalación

```bash
git clone <repo>
cd modelos_estadisticos

python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

pip install jupyter numpy pandas scikit-learn scipy matplotlib

jupyter notebook
```

---

## Ruta de aprendizaje sugerida

1. **Clases 1–4** — Leer el notebook completo, resolver todos los ejercicios 🟢 y al menos uno 🔴 por clase.
2. **Clases 5–7** — Implementar MLE manualmente, comparar umbrales con distintos costos.
3. **Clases 8–9** — Calcular el discriminante de Fisher a mano en datos 2D, comparar LDA vs QDA.
4. **Clases 10–11** — Construir el scree plot desde eigenvalores, nombrar componentes por sus loadings.
5. **Tarea 2** — Integrar PCA + Logística en un pipeline end-to-end sobre datos de crédito.

---

## Notas

- Todos los notebooks usan `np.random.seed(42)` para reproducibilidad.
- Las derivaciones asumen conocimiento previo de álgebra lineal, cálculo y estadística básica.
- Los notebooks están en español; los comentarios en código mezclan español e inglés.

---

<a name="english"></a>
# English

Repository for the **Statistical Models** course, covering linear regression, logistic regression, discriminant analysis, and dimensionality reduction. Each class includes a theory notebook with step-by-step mathematical derivations and an exercise notebook with progressive difficulty.

## Repository Structure

```
modelos_estadisticos/
├── Clase_1/          # Linear algebra and least squares
├── Clase_2/          # Eigendecomposition and distribution of β̂
├── Clase_3/          # Gauss-Markov assumptions and BLUE
├── Clase_4/          # Inference: R², ANOVA, t-tests
├── Clase_5/          # Logistic regression and MLE
├── Clase_6/          # Evaluation and diagnostics for logistic models
├── Clase_7/          # Optimal threshold and credit scoring
├── Clase_8/          # Linear Discriminant Analysis (LDA)
├── Clase_9/          # QDA and customer segmentation
├── Clase_10/         # PCA and SVD
├── Clase_11/         # Selection criteria and PCA interpretation
└── Tarea_2/          # Applied projects: credit risk + PCA
```

## Modules

### Module 1 — Linear Regression (Classes 1–4)

OLS foundations from matrix algebra through full statistical inference.

| Class | Topic | Key Concepts |
|-------|-------|--------------|
| **1** | Linear algebra and OLS | Normal equations XᵀX β = Xᵀy, hat matrix H, rank condition |
| **2** | Eigendecomposition and distribution of β̂ | Eigenvalues of XᵀX, multivariate normal distribution, variance of β̂ |
| **3** | Gauss-Markov and BLUE | 5 assumptions, unbiasedness, homoscedasticity, residual diagnostics |
| **4** | Inference and reporting | R², ANOVA table, F-test, t-tests, confidence intervals |

**Datasets:** California Housing, salary prediction.

**Functions built from scratch:** `ols_fit()`, `ols_summary()`, `ols_diagnostics()`, `describe_sigma()`

---

### Module 2 — Logistic Regression (Classes 5–7)

Binary classification via the generalized linear model.

| Class | Topic | Key Concepts |
|-------|-------|--------------|
| **5** | GLM and logit function | Why OLS fails for {0,1}, sigmoid function σ(z), MLE, gradient descent |
| **6** | Evaluation and diagnostics | Deviance vs SSE, AIC, Wald test (z-stats), McFadden Pseudo R², ROC/AUC |
| **7** | Threshold and scoring | Cost-based threshold selection, Logistic vs LDA, credit pipeline |

**Datasets:** Bank fraud detection, credit default.

---

### Module 3 — Discriminant Analysis (Classes 8–9)

Classification via maximization of between-class variance.

| Class | Topic | Key Concepts |
|-------|-------|--------------|
| **8** | LDA and Fisher's criterion | Matrices Sᵦ and Sᵥᵥ, linear boundaries, multiclass reduction |
| **9** | QDA and applications | Quadratic boundaries when Σₖ differs, confusion matrix per class |

**Datasets:** Customer segmentation (Family / Young Urban / Senior).

---

### Module 4 — Principal Component Analysis (Classes 10–11)

Unsupervised dimensionality reduction via variance maximization.

| Class | Topic | Key Concepts |
|-------|-------|--------------|
| **10** | PCA and SVD | Covariance eigendecomposition, SVD equivalence, scree plot, biplot |
| **11** | Selection and interpretation | Criteria: % variance, Kaiser, elbow; loadings; reconstruction error; pipeline |

**Datasets:** Financial data with 8 correlated features (income, debt, 30-day delinquency, 90-day delinquency, etc.)

---

### Tarea 2 — Applied Projects

| Notebook | Description |
|----------|-------------|
| `Clase07_Scoring_Threshold_CreditRisk.ipynb` | Full credit scoring pipeline with cost-based threshold optimization |
| `PCA_CreditRisk.ipynb` | PCA applied to credit data for feature reduction before classification |

---

## Class Structure

Each class contains two notebooks:

**Main notebook** (`ClaseXX_Topic.ipynb`)
- Complete mathematical derivations (not just formulas)
- NumPy implementation from scratch before using scikit-learn
- Real dataset with business-context interpretation
- Purpose-driven visualizations (ROC curves, scree plots, biplots, 3D surfaces)

**Exercise notebook** (`ClaseXX_Ejercicios.ipynb`)
- Progressive difficulty: 🟢 basic · 🟡 intermediate · 🔴 advanced
- Structure: problem statement → your code → reference solution
- Exercises chain together; the solution to one feeds into the next

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| Python 3.11 | Core language |
| NumPy | Linear algebra and matrix operations |
| Pandas | Tabular data manipulation |
| scikit-learn | Production models and evaluation |
| SciPy | Statistical distributions (t, F, χ²) |
| Matplotlib | Visualizations |

---

## Setup

```bash
git clone <repo>
cd modelos_estadisticos

python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

pip install jupyter numpy pandas scikit-learn scipy matplotlib

jupyter notebook
```

---

## Suggested Learning Path

1. **Classes 1–4** — Read each notebook end-to-end, complete all 🟢 exercises and at least one 🔴 per class.
2. **Classes 5–7** — Implement MLE manually, compare thresholds under different cost structures.
3. **Classes 8–9** — Compute Fisher's discriminant by hand on 2D data, compare LDA vs QDA.
4. **Classes 10–11** — Build the scree plot from eigenvalues directly, name components from loadings.
5. **Tarea 2** — Integrate PCA + Logistic Regression into an end-to-end pipeline on credit data.

---

## Notes

- All notebooks use `np.random.seed(42)` for reproducibility.
- Derivations assume prior knowledge of linear algebra, calculus, and basic statistics.
- Notebooks are written in Spanish; code comments mix Spanish and English.
