![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Desafío Empresarial: Análisis de Cohortes para los Pagos de Ironhack (Proyecto 1)

## Introducción

IronHack Payments, una empresa de servicios financieros de vanguardia, ha estado ofreciendo soluciones innovadoras de adelanto de efectivo desde su creación en 2020. Con un compromiso de proporcionar adelantos de dinero gratuitos y precios transparentes, IronHack Payments ha logrado una base de usuarios sustancial. Como parte de su esfuerzo continuo por mejorar sus servicios y entender el comportamiento de los usuarios, IronHack Payments ha encargado un proyecto de análisis de cohortes.

## Visión General del Proyecto

En este proyecto, realizarás un análisis de cohortes exhaustivo basado en datos proporcionados por IronHack Payments. El objetivo principal es analizar cohortes de usuarios definidos por el mes de creación de su primer adelanto en efectivo. Seguirás la evolución mensual de las métricas clave para estas cohortes, lo que permitirá a IronHack Payments obtener valiosas perspectivas sobre el comportamiento de los usuarios y el rendimiento de sus servicios financieros.

### Métricas a Analizar

Calcularás y analizarás las siguientes métricas para cada cohorte:

1. **Frecuencia de Uso del Servicio:** Comprender con qué frecuencia los usuarios de cada cohorte utilizan los servicios de adelanto de efectivo de IronHack Payments a lo largo del tiempo.
2. **Tasa de Incidentes:** Determinar la tasa de incidentes, enfocándose específicamente en los incidentes de pago, para cada cohorte. Identificar si hay variaciones en las tasas de incidentes entre diferentes cohortes.
3. **Ingresos Generados por la Cohorte:** Calcular el total de ingresos generados por cada cohorte a lo largo de los meses para evaluar el impacto financiero del comportamiento de los usuarios.
4. **Nueva Métrica Relevante:** Proponer y calcular una nueva métrica relevante que brinde perspectivas adicionales sobre el comportamiento de los usuarios o el rendimiento de los servicios de IronHack Payments.

### Herramientas de Análisis de Datos

Se espera que realices el análisis de cohortes utilizando Python, aprovechando principalmente la biblioteca Pandas para la manipulación y análisis de datos. Sin embargo, el análisis principal debe realizarse utilizando Python.

### Análisis Exploratorio de Datos (EDA)

Antes de sumergirte en el análisis de cohortes, realiza un análisis exploratorio de datos para obtener una comprensión completa del conjunto de datos. Explora estadísticas clave, distribuciones y visualizaciones para identificar patrones y valores atípicos. El EDA te ayudará a tomar decisiones informadas sobre estrategias de preprocesamiento y análisis de datos.

### Análisis de la Calidad de Datos

Evalúa la calidad del conjunto de datos identificando valores faltantes, inconsistencias en los datos y posibles errores. Implementa pasos de limpieza y preprocesamiento de datos para garantizar la fiabilidad de tu análisis. Documenta cualquier problema de calidad de datos encontrado y los pasos tomados para abordarlos.

### Entregables

1. **Código en Python:** Proporciona código en Python bien documentado que realice el análisis de cohortes, incluyendo la carga de datos, preprocesamiento, creación de cohortes, cálculo de métricas y visualización.
2. **Informe de Análisis Exploratorio de Datos:** Prepara un informe que resuma los hallazgos de tu análisis exploratorio de datos. Incluye visualizaciones e insights que ayuden a entender el conjunto de datos.
3. **Informe de Análisis de la Calidad de Datos:** Documenta los resultados de tu análisis de calidad de datos, destacando cualquier problema y los pasos tomados para resolverlos.
4. **Presentación Corta:** Crea una presentación concisa (máximo de 4 diapositivas) que resuma tus hallazgos del análisis de cohortes y las perspectivas clave obtenidas del EDA y el análisis de calidad de datos. Esta presentación debe ser adecuada para compartir con el equipo de IronHack Payments.

# Solución del proyecto

## Estructura del proyecto

```bash
.
├── Entorno Personal
│   ├── Alejandro
│   │   ├── EDA_cash.ipynb
│   │   ├── EDA_fees.ipynb
│   │   ├── historia_analisis_cohortes.ipynb
│   │   └── ingresos_por_cohorte.ipynb
│   ├── Anastasia
│   │   ├── cash2.ipynb
│   │   ├── cash.ipynb
│   │   ├── fees.ipynb
│   │   └── join.ipynb
│   ├── Marc
│   │   ├── Analisis Exploratorio CASH.ipynb
│   │   ├── Analisis Exploratorio FEE.ipynb
│   │   ├── joined (còpia).ipynb
│   │   ├── joined.ipynb
│   │   ├── unio.xlsx
│   │   └── Untitled.ipynb
│   └── Toni
│       └── AnalisisCASH.ipynb
├── Notebooks
│   ├── analisis amount vs return_days_diff.ipynb
│   └── ingresos_por_cohorte.ipynb
├── project_dataset
│   ├── cash_request.csv
│   ├── fees_data.csv
│   └── Lexique - Data Analyst.xlsx
└── readme.md

```

## Devtools

Herramientas necesarias para la ejecución del código:

```
Python 3.10.12
Jupyter notebook
```

Módulos python necesarios:

```
matplotlib==3.8.4
numpy==1.26.4
pandas==2.2.2
plotly==5.22.0
seaborn==0.13.2
```

## Análisis realizados

### Ingresos de fees por cohorte:

Hemos identificado que los ingresos por comisiones se generan a partir de mayo de 2020. Esto sugiere una posible actualización en la plataforma, introduciendo comisiones en ciertas acciones.

Con esta información en mente, hemos enfocado nuestro análisis en las transacciones con estatus **money_back** (devolución de dinero completada).

A continuación, se presenta un análisis detallado de los ingresos generados por mes.

```
cohorte_month        Dinero adelantado por cohorte        Ingresos por cohorte
2019-11                          131.0                          30.0
2019-12                          65298.0                        1100.0
2020-01                          20836.0                        455.0
2020-02                          31442.0                        635.0
2020-03	                         7690.0                         610.0
2020-04	                         60712.0                        1525.0
2020-05                          111872.0                       3780.0
2020-06                          311324.0                       13870.0
2020-07                          201434.0                       10695.0
2020-08                          67385.0                        4925.0
2020-09                          141138.0                       11185.0
2020-10                          311375.0                       23220.0
2020-11                          5510.0                         320.0`
```

## Conclusiones