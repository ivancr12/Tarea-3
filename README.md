Tarea 3 - Computación Paralela y Distribuida

Descripción del problema

El objetivo de esta tarea es predecir la severidad de accidentes de tránsito en Estados Unidos utilizando el dataset US Accidents. Se implementó un pipeline completo de análisis de datos y machine learning usando Polars, comparando su rendimiento con Pandas.

Fuente del dataset

Nombre: US Accidents (March 2023)
Plataforma: Kaggle
Registros: 7,728,394
Columnas: 46
Variable objetivo: Severity (1-4)
Requisitos de software

Python 3.12+
Polars 1.35.2
Pandas
Scikit-learn
Matplotlib
Seaborn
NumPy
psutil
Instalación

text
pip install polars pandas scikit-learn matplotlib seaborn numpy psutil
Instrucciones de ejecución

Clonar el repositorio:
text
git clone https://github.com/ivancr12/Tarea-3.git
cd Tarea-3
Descargar el dataset US_Accidents_March23.csv desde Kaggle y colocarlo en la carpeta del proyecto.
Abrir el notebook Tarea_3.ipynb en Google Colab o Jupyter Notebook.
Ejecutar las celdas en orden.
Estructura del repositorio

text
Tarea-3/
├── README.md
├── Tarea_3.ipynb
├── requirements.txt
├── figures/
│   ├── benchmark_tiempos.png
│   ├── benchmark_speedup.png
│   ├── escalabilidad.png
│   ├── lazy_vs_eager.png
│   └── severity_distribution.png
└── data/
    └── US_Accidents_March23.csv
Resumen de resultados

Machine Learning

Modelo	Accuracy	F1-Score	Tiempo
Logistic Regression	79.63%	0.7060	52s
Random Forest	79.17%	0.7237	18s
Gradient Boosting	79.60%	0.7098	64s
Mejor modelo: Random Forest

Benchmark Polars vs Pandas

Operación	Speedup
Carga	21.99x
Agregación	2.34x
Pipeline	2.12x
Join	1.51x
Lazy Execution

Speedup: 1.43x (Lazy fue más rápido)
Escalabilidad

Polars mostró mejor rendimiento en datasets grandes, alcanzando speedups de hasta 7.57x.

Conclusiones

Polars es significativamente más rápido que Pandas en carga de datos (21.99x).
La ejecución diferida (Lazy) mejora el rendimiento en 1.43x.
Random Forest fue el mejor modelo predictivo.
El beneficio de Polars aumenta con el tamaño del dataset.
