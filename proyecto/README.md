# Proyecto final Boyacá · Big Data

source .venv/bin/activate

pip install -r requirements.txt

./run_pipeline.sh


## Otra manera

Ejecutar los notbooks del 1 al 8 que se encuentran en el directorio "notebooks"

```
proyecto_boyaca/
├── staging/                 # los 6 archivos originales, con su nombre de descarga
├── data_lake/
│   ├── bronze/<fuente>/     # <fuente>.csv (GeoJSON -> CSV con WKT) + manifest.json
│   ├── silver/              # Parquet / GeoParquet validados
│   ├── gold/                # tablas analíticas
│   └── rejects/             # filas rechazadas con su motivo
├── src/                     # toda la lógica (ver tabla de abajo)
├── notebooks/               # 01 … 08: llaman a src/ en orden
├── tests/                   # pytest: unitarias (sin datos) + de capas (con datos)
├── outputs/{quality,stats,figures,maps,logs}
├── requirements.txt
└── run_pipeline.sh
```
