# End-to-End E-commerce ETL & Data Warehouse Pipeline

## Overview

This project implements a production-style ETL pipeline integrating three different data sources:

- Transactional B2B commerce database  
- Apache web server logs (combined format)  
- Marketing leads Excel spreadsheet  

The pipeline loads the data into a star-schema data warehouse designed for analytical reporting.

---

## Architecture

Sources → Python ETL Layer → Star Schema Warehouse → Reporting

- B2B Transactional DB  
- Web Logs  
- Marketing Spreadsheet  
            ↓  
Python ETL Pipeline (Validation, Checkpointing, Error Logging)  
            ↓  
Fact & Dimension Tables  
            ↓  
Analytical Queries  

---

## Key Features

- Initial and incremental loading  
- Checkpoint-based restartability  
- Batch processing for scalability  
- Row-level validation with structured error logging  
- ETL metadata tracking (run status, steps, failures)  
- Device parsing using user-agent extraction  
- Date dimension generation  

---

## Reporting Supported

- Top 5 most used devices  
- Most popular products by highest-login country  
- Monthly sales performance (last 12 months)  

---

## Technologies Used

- Python  
- Pandas  
- SQL  
- SQLite  
- Regex  

---

## Scalability

- 300K+ transactional records processed  
- 250K+ web events processed  
- Batch-based ingestion with checkpoint recovery  
