# Modelo de predicción de pobreza en hogares peruanos utilizando ENAHO

## Problema

Programas sociales como Juntos y Pensión 65 necesitan identificar adecuadamente a los hogares que forman parte de su población objetivo. Esta investigación explora modelos de aprendizaje automático para identificar hogares en situación de pobreza y estudiar los errores de exclusión.

## Pregunta de investigación

¿Cuál de los cuatro modelos evaluados (regresión logística, árbol de decisión, KNN y perceptrón multicapa) identifica con menor error de exclusión a los hogares en situación de pobreza, a una cobertura comparable, a partir de características socioeconómicas observables de ENAHO?

## Hipótesis

Los modelos no lineales (árbol de decisión, KNN y perceptrón multicapa) no reducen de forma significativa el error de exclusión respecto a la regresión logística regularizada al evaluarlos a una cobertura comparable, debido a que la relación entre las características socioeconómicas observables y la condición de pobreza es en gran parte aproximadamente lineal.

## Objetivos

### Objetivo general

Desarrollar y comparar regresión logística, árbol de decisión, vecinos más cercanos y perceptrón multicapa para identificar hogares en situación de pobreza a partir de características socioeconómicas observables de ENAHO, evaluando cuál reduce más el error de exclusión.

### Objetivos específicos

- Definir la variable objetivo a partir de la condición de pobreza (pobre/no pobre) de ENAHO.
- Seleccionar características socioeconómicas observables, excluyendo gasto e ingreso para evitar fuga de información.
- Preparar los datos mediante limpieza, tratamiento de valores faltantes, codificación y escalamiento.
- Implementar y ajustar los cuatro modelos.
- Comparar los modelos mediante error de exclusión a cobertura comparable, sensibilidad, precisión y F1.
- Analizar los falsos negativos.

## Tecnologías

El proyecto usa Python y las dependencias listadas en `requirements.txt`: pandas, NumPy, Matplotlib, Seaborn, scikit-learn, Jupyter, ipykernel y openpyxl.

## Estructura actual

```text
.
├── data/
│   ├── raw/                  # Archivos ENAHO y documentación originales, de uso local
│   ├── interim/              # Archivos intermedios
│   ├── processed/
│   │   ├── resultados/       # Métricas, predicciones y modelos generados
│   │   ├── tablas_limpias/   # Tablas preparadas por módulo
│   │   └── trazabilidad/     # Registros de filas y exclusiones
│   └── README.md             # Organización y manejo de los datos
├── notebooks/
│   ├── 01_exploracion_datos.ipynb
│   ├── 02_limpieza_datos.ipynb
│   ├── 03_base_hogar.ipynb
│   ├── 04_particion_por_conglomerado.ipynb
│   └── 05_modelos.ipynb
├── reports/
│   └── figures/              # Figuras para reportes
├── requirements.txt
├── .gitignore
└── README.md
```
