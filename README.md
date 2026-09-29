# Microsoft Fabric End-to-End Data Engineering Project

An end-to-end data engineering project built using **Microsoft Fabric**, implementing a **Medallion Architecture (Bronze, Silver, and Gold layers)** to ingest, transform, and prepare data for downstream analytics.

## Project Overview

This project demonstrates how Microsoft Fabric can be used to build a structured data pipeline covering data ingestion, transformation, and analytics-ready data preparation.

The solution follows the Medallion Architecture:

**Source Data → Bronze Layer → Silver Layer → Gold Layer → Analytics**

- **Bronze Layer:** Ingests and stores raw source data using Microsoft Fabric Copy Job and Data Pipeline.
- **Silver Layer:** Cleans, validates, and transforms the raw data using a Fabric notebook.
- **Gold Layer:** Creates curated, analytics-ready datasets for downstream reporting and analysis.

## Technologies

- Microsoft Fabric
- Fabric Data Factory
- Fabric Data Pipelines
- Fabric Lakehouse
- PySpark
- Python
- SQL
- Jupyter Notebooks
- Medallion Architecture

## Repository Structure

```text
microsoft-fabric-data-platform/
│
├── 01-copyjob-bronze-layer.json
├── 02-pipeline-bronze-layer.json
├── 03-ntb-silver-layer.ipynb
├── 04-ntb-gold-layer.ipynb
└── README.md
```

### `01-copyjob-bronze-layer.json`

Defines the Microsoft Fabric Copy Job used for data ingestion into the Bronze layer.

### `02-pipeline-bronze-layer.json`

Contains the Fabric Data Pipeline configuration used to orchestrate the Bronze-layer ingestion workflow.

### `03-ntb-silver-layer.ipynb`

Processes Bronze-layer data and performs cleaning and transformation to create structured Silver-layer datasets.

### `04-ntb-gold-layer.ipynb`

Transforms curated Silver-layer data into Gold-layer datasets optimized for analytics and downstream consumption.

## Architecture

```text
                    Source Data
                         │
                         ▼
              Fabric Copy Job / Pipeline
                         │
                         ▼
                  ┌─────────────┐
                  │   BRONZE    │
                  │  Raw Data   │
                  └──────┬──────┘
                         │
                         ▼
                  PySpark Notebook
                         │
                         ▼
                  ┌─────────────┐
                  │   SILVER    │
                  │ Clean Data  │
                  └──────┬──────┘
                         │
                         ▼
                  Transformation
                         │
                         ▼
                  ┌─────────────┐
                  │    GOLD     │
                  │ Analytics   │
                  └──────┬──────┘
                         │
                         ▼
                Downstream Analytics
```

## Key Features

- End-to-end data engineering workflow using Microsoft Fabric
- Medallion Architecture with Bronze, Silver, and Gold layers
- Automated data ingestion using Fabric Copy Job and Data Pipelines
- Data cleaning and transformation using PySpark notebooks
- Structured transformation from raw to analytics-ready datasets
- Reusable pipeline and notebook components
- Foundation for downstream BI and analytics workloads

## Purpose

The project was developed to gain hands-on experience designing an end-to-end data platform using Microsoft Fabric and modern data-engineering practices, with particular focus on pipeline orchestration, Lakehouse architecture, PySpark transformations, and layered data modelling.
