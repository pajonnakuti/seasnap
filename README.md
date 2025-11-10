# 🌊 SeaSnap

**From Raw CTD Data to Geospatial Insights and Argo Float Context**

SeaSnap is a comprehensive data pipeline and visualization platform for Conductivity, Temperature, and Depth (CTD) data. The project streamlines the transformation of raw CTD files into structured datasets, applies rigorous quality control, and presents interactive geospatial analytics via a web dashboard.

## Features

- **Multi-format Data Ingestion**  
  Supports parsing and extraction from various raw CTD file formats, including:
  - `.cnv`
  - `.asci`
  - `.xls`
  - `.dat`

- **Data Structuring**  
  Converts extracted data into structured tables suitable for analysis and visualization.

- **Quality Control**  
  Implements quality control mechanisms inspired by Argo float data standards.  
  - Assigns QC flags to each parameter (e.g., temperature, salinity, conductivity).

  - 📈 QC Flags (Based on ARGO Standards)
    - Each parameter is assigned a quality flag:
      - 1: Good data
      - 2: Probably good
      - 3: Probably bad
      - 4: Bad data
      - 9: Missing value
      
- **Geospatial Visualization & Analytics**  
  - Interactive maps and plots to explore CTD data spatially and temporally.
  - Available plots include:
    - **Depth vs Temperature**
    - **Depth vs Salinity**
    - **Depth vs Conductivity**
    - **Temperature-Salinity (TS) plots**

- **Web Dashboard**  
  A live web application (using a live server) presents all CTD data and analytics in an accessible dashboard format.

## Getting Started

### Prerequisites

- Python 3.x
- Required libraries (see `requirements.txt`)
- (Optional) Node.js or another live-server tool for hosting the dashboard

### Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/pajonnakuti/seasnap.git
    cd seasnap
    ```

2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **(Optional) Start the live server**  
   For the dashboard:
    ```bash
    # Example using Python's http.server
    python -m http.server 8000
    ```

### Usage

1. **Place your raw CTD files** in the designated input directory.
2. **Run the extraction and structuring scripts** to process the data.
3. **Perform automated quality control (QC) on the processed data** following Argo float standards to ensure accuracy and reliability.
4. **Visualize the cleaned and structured datasets** through interactive geospatial maps and charts using the web dashboard for clear insights into oceanographic measurements.

