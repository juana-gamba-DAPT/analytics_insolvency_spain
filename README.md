## Insolvencia (Ley de Segunda Oportunidad) en España desde 2021

**Propósito**: Este proyecto busca analizar la situación de la insolvencia en España, a partir de 2021, para generar un dashboard (Google Looker Studio) que apoye la toma de decisiones en despachos especializados en liquidación de deudas.
El objetivo principal es identificar tendencias, perfiles y patrones que permitan a estos despachos:
-Decidir dónde abrir nuevas oficinas.
-Orientar campañas de captación.
.Reconocer los perfiles de clientes con mayor probabilidad de necesitar este servicio.

**Alcance del análisis**
El dashboard incluye:
Perfiles demográficos y socioeconómicos de los deudores (empresas vs personas físicas; tamaño, facturación, antigüedad).
Distribución geográfica de los casos (por comunidad autónoma y provincia).
Evolución temporal de los concursos y de la Ley de Segunda Oportunidad (2021–2025T2).

## Datos
- **Registradores de España**: bases trimestrales con información desde 2021T1 hasta 2025T2.
EPC1: sociedades concursadas.
EPC2: personas físicas concursadas.
EPC3: tipo de procedimiento.
EPC4: tipo de concurso (ordinario/especial/sin masa).
EPC5: número de empleados.
EPC6: volumen de negocio y antigüedad.
- INE / Banco de España: indicadores macroeconómicos de referencia (PIB, paro).

👉 Nota: de momento, los datos centrales son los de los Registradores. Las demás fuentes están consideradas para enriquecer el análisis más adelante.

## Pipeline
1. Carga de archivos CSV (EPC1–EPC6).
2. Limpieza: eliminación de columnas de totales duplicados, renombrado de variables, control de valores nulos.
3. Unión de datasets por provincia, año y trimestre (consolidación en merged_registradores).
4. EDA (Análisis exploratorio):
Estadísticas descriptivas.
Validación de consistencia (promedio de concursos por periodo, outliers).
Visualizaciones iniciales (tipos de concursos, distribución geográfica, evolución temporal).
5. Modelo de datos: preparación de métricas clave (KPIs) para el dashboard.
6. Dashboard interactivo en Google Looker Studio


## KPIs
- Nº casos por año/CA y por tipo (voluntario/necessario/consecutivo).
- % composición por tipo de sociedad (SL, SA, otros) y personas físicas.
- Distribución por empleados, volumen de negocio y antigüedad.

## Recursos adicionales

- 📊 [Dashboard en Looker Studio](https://lookerstudio.google.com/reporting/2608eeec-c38e-4568-a832-eead923c14f4)  
- 📝 [Presentación del proyecto (Canva)](https://www.canva.com/design/DAGxAKuIEq0/BThCJo9v71uinsS6AgVOCg/edit?utm_content=DAGxAKuIEq0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)  
- 📌 [Tablero de trabajo en Trello](https://trello.com/invite/b/68a70e0e7bb56f6c4b04fee6/ATTI02f529c449a418e3512e72153557fb87710CAC33/liquideudaproject)  
- 📂 [Otros](https://drive.google.com/xxxx)  


## Requisitos
-Python 3.10+
-Librerías: pandas, numpy, matplotlib, seaborn, jupyter
-Google Looker Studio para el dashboard


**👩‍💻 Autor**
Proyecto desarrollado como primer trabajo de Data Analyst:

- Nombre: Juana Gabriela Gamba
- LinkedIn: [gabrielagambap](https://www.linkedin.com/in/gabrielagambap-industrialengineer/)  
- Email: juana.gabriela21@gmail.com  

**Licencia**

Este proyecto se distribuye bajo la licencia MIT
