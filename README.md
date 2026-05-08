# 📊 HR Employee Attrition Analysis / Análisis de Rotación de Empleados

---

## 🇪🇸 Español

### Descripción

Análisis exploratorio de datos (EDA) sobre el dataset **IBM HR Analytics Employee Attrition & Performance**. El objetivo es identificar los factores clave que impulsan la rotación de empleados y generar insights accionables para el departamento de Recursos Humanos.

### Dataset

- **Fuente:** IBM HR Analytics (Kaggle)
- **Registros:** 1,470 empleados
- **Variables:** 35 columnas (demográficas, laborales, de satisfacción y rendimiento)
- **Variable objetivo:** Attrition (Yes/No)

### Estructura del Análisis

1. **Exploración inicial** — Dimensiones, tipos de datos, valores nulos y estadísticas descriptivas.
2. **Variables categóricas** — Distribución de BusinessTravel, Department, JobRole, EducationField, Gender, MaritalStatus y OverTime.
3. **Distribuciones y comparaciones** — Histogramas de antigüedad (YearsAtCompany, YearsWithCurrManager, YearsInCurrentRole, YearsSinceLastPromotion), distribución de edad por Attrition, evolución salarial por género y edad.
4. **Análisis de proporciones** — Tasa de rotación por OverTime, Department, JobRole, Gender y cruce de OverTime × WorkLifeBalance.
5. **Correlaciones (Spearman)** — Matriz de variables relacionadas con el puesto y matriz de variables de rendimiento/satisfacción.

### Hallazgos Principales

- **OverTime es el predictor más fuerte de rotación** (ρ = 0.25). Los empleados que hacen horas extra tienen una tasa de rotación significativamente más alta.
- **El rendimiento no predice la rotación** (ρ = 0.00). La empresa pierde tanto buenos como malos performers, lo que indica que el problema no es de bajo rendimiento sino de condiciones laborales.
- **La mayoría de las bajas ocurren en el primer año con el manager actual** (~80 empleados), lo que sugiere un posible problema de onboarding o integración temprana.
- **Salario bajo + nivel bajo = mayor rotación.** MonthlyIncome (ρ = -0.20) y JobLevel (ρ = -0.19) están negativamente correlacionados con la rotación.
- **OverTime combinado con mal WorkLifeBalance es la combinación más tóxica**, disparando la tasa de rotación muy por encima de lo esperado por cada factor individual.
- **Las variables de satisfacción son independientes entre sí.** JobSatisfaction, EnvironmentSatisfaction, WorkLifeBalance y JobInvolvement miden dimensiones distintas y no se pueden tratar como intercambiables.
- **DailyRate, HourlyRate y MonthlyRate no aportan valor predictivo** — no correlacionan con ninguna variable relevante.

### Tecnologías

- Python 3
- Pandas
- Seaborn
- Matplotlib
- NumPy
- Google Colab

### Cómo Ejecutar

1. Abrir el notebook `HR_Analysis.ipynb` en Google Colab o Jupyter Notebook.
2. Descargar el dataset de [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) y colocarlo en la ruta correspondiente.
3. Ejecutar todas las celdas.

---

## 🇬🇧 English

### Description

Exploratory Data Analysis (EDA) on the **IBM HR Analytics Employee Attrition & Performance** dataset. The goal is to identify the key drivers of employee turnover and generate actionable insights for the HR department.

### Dataset

- **Source:** IBM HR Analytics (Kaggle)
- **Records:** 1,470 employees
- **Features:** 35 columns (demographics, job-related, satisfaction, and performance)
- **Target variable:** Attrition (Yes/No)

### Analysis Structure

1. **Initial exploration** — Shape, data types, null values, and descriptive statistics.
2. **Categorical variables** — Distribution of BusinessTravel, Department, JobRole, EducationField, Gender, MaritalStatus, and OverTime.
3. **Distributions and comparisons** — Tenure histograms (YearsAtCompany, YearsWithCurrManager, YearsInCurrentRole, YearsSinceLastPromotion), age distribution by Attrition, salary evolution by gender and age.
4. **Proportion analysis** — Attrition rate by OverTime, Department, JobRole, Gender, and OverTime × WorkLifeBalance cross-analysis.
5. **Correlations (Spearman)** — Correlation matrix for role-related variables and performance/satisfaction variables.

### Key Findings

- **OverTime is the strongest predictor of attrition** (ρ = 0.25). Employees working overtime have a significantly higher turnover rate.
- **Performance does not predict attrition** (ρ = 0.00). The company loses both high and low performers, indicating the issue is not poor performance but working conditions.
- **Most departures happen within the first year with the current manager** (~80 employees), suggesting a potential onboarding or early integration problem.
- **Low salary + low job level = higher attrition.** MonthlyIncome (ρ = -0.20) and JobLevel (ρ = -0.19) are negatively correlated with turnover.
- **OverTime combined with poor WorkLifeBalance is the most toxic combination**, pushing the attrition rate well above what either factor alone would predict.
- **Satisfaction variables are independent of each other.** JobSatisfaction, EnvironmentSatisfaction, WorkLifeBalance, and JobInvolvement measure distinct dimensions and cannot be treated as interchangeable.
- **DailyRate, HourlyRate, and MonthlyRate have no predictive value** — they don't correlate with any relevant variable.

### Tech Stack

- Python 3
- Pandas
- Seaborn
- Matplotlib
- NumPy
- Google Colab

### How to Run

1. Open `HR_Analysis.ipynb` in Google Colab or Jupyter Notebook.
2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) and place it in the appropriate path.
3. Run all cells.

---

## 📁 Project Structure

```
hr-attrition-analysis/
│
├── HR_Analysis.ipynb       # Main analysis notebook
├── data-raw/               # Raw dataset (not included, download from Kaggle)
├── README.md               # This file
```

## 📝 License

This project is for educational and portfolio purposes. The dataset is provided by IBM via Kaggle.
