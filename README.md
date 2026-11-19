# EASE-6G reproducibility package

Code, data and results for the article:

**When Does Carbon-Aware AI Inference Placement Pay? A Closed-Form Regime Analysis across the Edge–Cloud Continuum and Design Rules for 6G Compute Placement**
Ahmed Mostafa Saleh ElSawaf, Nour Eldeen M. Khalifa, Mohamed Hamed N. Taha and Shaimaa M. Mohamed
Submitted to *Future Internet* (MDPI), 2026.

## Contents

`EASE6G_Final_Package_MDPI.zip` holds the complete package:

- Python implementation of the model and all experiments, with solver configurations
- parameter tables (Tables 3–5 of the article)
- frozen 2026 NESO regional carbon-intensity traces with retrieval metadata
- the MLPerf performance and power logs behind the efficiency inputs
- all numerical results, an independent check of every equation, and the figure scripts
- `MANIFEST.sha256`, a checksum for every file

## Reproduce

    unzip EASE6G_Final_Package_MDPI.zip && cd EASE6G_Final_Package
    pip install -r code/requirements.txt      # pandoc must be on PATH
    bash code/run_v2.sh manuscript/source/source_manuscript.docx manuscript/source/source_manuscript.md /tmp/rebuilt.docx

One command regenerates every result, table and figure and rebuilds the manuscript in about three minutes on one core. `README.md` inside the package describes each script and output.
