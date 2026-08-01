# theoutliers-taller-practico-03

## Inteligencia Geo-Temporal y de Redes — Optimización de Activos Críticos: TechLogistics S.A.

Challenge 02 (Analítica Multidimensional) — EAFIT, Maestría en Ciencia de Datos y
Analítica, Periodo 2026-1. Docente: Jorge Iván Padilla-Buriticá.

## Contexto de negocio

TechLogistics S.A. (empresa ficticia) enfrenta un problema de visibilidad: los datos de
su cadena de frío (sensores agroindustriales) y de su red eléctrica están
georreferenciados pero desconectados entre sí. Este proyecto integra tres capas de
análisis para dar soporte a la junta directiva:

1. **Grafos** — cómo se propaga el ruido/telemetría en la red de sensores y
   subestaciones.
2. **Geoespacial** — dónde se localizan los puntos críticos de calor y biomasa baja.
3. **Series de Tiempo** — cuál es el pronóstico de carga y el impacto del ruido de
   sensores sobre los modelos predictivos.

## Estructura del repositorio

```
.
├── README.md
├── data/                          # Datasets agro_*.csv y ener_*.csv
├── notebooks/
│   └── taller_practico_03_analisis.ipynb   # Notebook principal del análisis
├── src/                           # Funciones auxiliares reutilizables (opcional)
├── results/
│   └── figuras/                   # Gráficas exportadas como evidencia
└── docs/
    └── declaracion_uso_IA.md      # Declaración de uso de herramientas de IA
```

## Datasets

- `data/agro_clean.csv` / `data/agro_noise.csv`: sensores mesh agroindustriales
  (hídricas, radiación PAR, índices bióticos, suelo/viento, geolocalización y topología
  de red del cultivo).
- `data/ener_clean.csv` / `data/ener_noise.csv`: red eléctrica nacional simulada
  (mercado spot, generación eólica, factores macro, calidad de potencia,
  geolocalización y topología de despacho).

Las versiones `noise` incluyen ruido gaussiano aditivo (AWGN) inyectado sobre las
señales y jitter en las coordenadas GPS, para evaluar técnicas de filtrado y
reconstrucción.

## Cómo reproducir el análisis

1. Crear un entorno virtual e instalar dependencias:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   ```
2. Abrir `notebooks/taller_practico_03_analisis.ipynb` y ejecutar las celdas en orden.

## Hallazgos principales

_Pendiente — se completa al cierre del análisis._

## Uso de herramientas de IA

Ver [`docs/declaracion_uso_IA.md`](docs/declaracion_uso_IA.md).
