# Azure Databricks E-Surveillance Email Compliance

This repository contains a production-ready starter for an **e-surveillance email compliance pipeline**
implemented on **Azure Databricks**. It includes example notebooks, a sample lexicon, sample data,
and modular Python code suitable for Databricks Repos and Databricks Workflows.

## Contents
- notebooks/: Databricks-ready Python notebooks (1-4) implementing Bronze→Silver→Gold.
- modules/: Reusable PySpark modules (email parsing, lexicon engine, preprocessing).
- lexicon/: Sample lexicon JSON.
- sample_data/: Small NDJSON sample emails to run locally or in Databricks.
- configs/: env-specific config templates.
- jobs/: sample Databricks job definitions (JSON).
- docs/: architecture diagram placeholder and README.

## Quickstart (Dev)
1. Upload `lexicon/lexicon.json` to your ADLS config container or point LEXICON_PATH to it.
2. Upload sample NDJSON to your ADLS raw container or use the sample_data file.
3. Import notebooks into Databricks or run from Databricks Repos.
4. Run notebooks in order: `01_bronze_ingest.py` -> `02_silver_clean_tokenize.py` -> `03_gold_lexicon_score.py`.
