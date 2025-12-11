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
├── data/ # Contains roi.geojson 
├── notebooks/ # Jupyter Notebooks (Analysis code) 
├── output/ # Generated PNG maps 
├── reports/ # Final PDF Report 
├── requirements.txt # Python dependencies 
└── README.md

## How to Run
1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd imagery-analyst-project
    ```

2.  **Install Dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Analysis:**
    Open the notebook `notebooks/workflow.ipynb` in Jupyter and run all cells.

4.  **View Results:**
    Check the `output/` directory for the generated change detection maps.

## Methodologies
* **Optical:** Utilizes the SWIR band (B11) to highlight concrete and asphalt.
* **SAR:** Utilizes VV polarization for hard-target detection (double-bounce) and VH for volume scattering context.
