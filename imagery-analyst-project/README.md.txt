# Urban Expansion Monitoring: Trivandrum (Sentinel-1 & Sentinel-2)

## Project Overview
This repository contains an automated workflow to monitor urban expansion, specifically analyzing the construction of the Lulu Mall complex in Trivandrum, India. The analysis spans from **2017 (Pre-construction)** to **2024 (Operational)**.

The tool uses a multi-sensor approach (Optical + SAR) to ensure robust detection regardless of cloud cover or surface ambiguity.

## Key Features
* **Automated Data Ingestion:** Uses Microsoft Planetary Computer STAC API to fetch Sentinel-2 (L2A) and Sentinel-1 (RTC) data.
* **Dual-Sensor Analysis:**
    * **Optical:** NDBI (Normalized Difference Built-up Index) change detection.
    * **SAR:** Dual-polarization (VV+VH) Log-Ratio change detection.
* **Dynamic Coregistration:** Automatically aligns disparate datasets to EPSG:32643 (UTM Zone 43N).
* **Professional Visualization:** Generates overlay maps and False Color Composites (FCC).

## Repository Structure