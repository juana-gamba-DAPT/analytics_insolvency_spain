## Insolvencia (Ley de Segunda Oportunidad) en España desde 2021

**Propósito**: Este proyecto busca analizar la situación de la insolvencia en España, a partir de 2021, para generar un dashboard interactivo (Google Looker Studio) que apoye la toma de decisiones en despachos especializados en liquidación de deudas.
El objetivo principal es identificar tendencias, perfiles y patrones que permitan a estos despachos:
-Decidir dónde abrir nuevas oficinas.
-Orientar campañas de captación.
.Reconocer los perfiles de clientes con mayor probabilidad de necesitar este servicio.

**Alcance del análisis**
El dashboard incluye:
Perfiles demográficos y socioeconómicos de los deudores (empresas vs personas físicas; tamaño, facturación, antigüedad).
Distribución geográfica de los casos (por comunidad autónoma y provincia).
Tiempos medios de resolución judicial (fuente CGPJ).
Evolución temporal de los concursos y de la Ley de Segunda Oportunidad (2021–2025T2).

## Datos
- **Registradores de España**: bases trimestrales con información desde 2021T1 hasta 2025T2.
EPC1: sociedades concursadas.
EPC2: personas físicas concursadas.
EPC3: tipo de procedimiento.
EPC4: tipo de concurso (ordinario/especial/sin masa).
EPC5: número de empleados.
EPC6: volumen de negocio y antigüedad.
- CGPJ: duración media de procesos judiciales.
- INE / Banco de España: indicadores macroeconómicos de referencia (PIB, paro, tipos de interés).

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
6. Dashboard interactivo en Google Looker Studio / Power BI.


## KPIs
- Nº casos por año/CA y por tipo (voluntario/necessario/consecutivo).
- % composición por tipo de sociedad (SL, SA, otros) y personas físicas.
- Tiempos medios de resolución por CA (días/meses).
- Distribución por empleados, volumen de negocio y antigüedad.
- Variación interanual.

## Requisitos
-Python 3.10+
-Librerías: pandas, numpy, matplotlib, seaborn, jupyter
-Google Looker Studio para el dashboard

👩‍💻 Autor
Proyecto desarrollado como primer trabajo de Data Analyst:
- Nombre: Juana Gabriela Gamba
- LinkedIn: [linkedin](https://www.linkedin.com/in/gabrielagambap-industrialengineer/)  
- Email: juana.gabriela21@gmail.com  

📜 Licencia
Este proyecto se distribuye bajo la licencia MIT
