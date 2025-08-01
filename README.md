# MixedPalletBoxes

![MIT License](https://img.shields.io/badge/license-MIT-green.svg)
![Python](https://img.shields.io/badge/python-3.7%2B-blue.svg)
![Languages Size](https://img.shields.io/github/languages/code-size/Adamos-Daios/package-db-distributions)
![Last Commit](https://img.shields.io/github/last-commit/Adamos-Daios/package-db-distributions)
![Issues](https://img.shields.io/github/issues/Adamos-Daios/package-db-distributions.svg)


A Synthetic Benchmark Dataset for Warehouse Applications.

---

## 📦 Key Features

* **Material Diversity**: Generates boxes made of Cardboard, Plastic, Wood, Metal, and Composite.
* **Dimensional Randomization**: Random lengths, widths, heights, and thicknesses within material-specific ranges.
* **Property Calculation**: Computes external/internal volumes and max load capacity.
* **Attribute Flags**: Assigns fragile, stackable, waterproof, and fire-retardant flags.
* **Environmental Ranges**: Random safe temperature limits for each material.
* **Metadata**: Includes box color and country of origin.

---

## ⚙️ Setup

1. **Clone repo**

   ```bash
   git clone https://github.com/your-username/box-database-generator.git
   cd box-database-generator
   ```
2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```
Note: This will install pandas and openpyxl, required for generating Excel files.
---

## ▶️ Usage

* Open [box_generator.py](./box_generator.py).
* Set the desired number of records (default: 10,000).
* Run:

  ```bash
  python generate_boxes.py
  ```
* Result: `boxes_database.xlsx` saved in the working directory.

---
📁 Pre-Generated Datasets
A collection of ready-to-use Excel datasets is available in the boxes_database/ folder. These files include:

boxes_500.xlsx

boxes_1000.xlsx

boxes_3000.xlsx

boxes_5000.xlsx

boxes_10000.xlsx

boxes_50000.xlsx

boxes_100000.xlsx

Each file contains a fixed number of randomly generated box records, following the same structure.

## 📂 Example Dataset

Download a sample box dataset with 10,000 records:

[📥 Download boxes__database_10.000.xlsx](https://github.com/Adamos-Daios/package-db-distributions/raw/main/boxes_database/boxes_database_10.000.xlsx?raw=true)


---
## 📊 Sample Dataset Preview

Each Excel file contains records with the following structure:

| Box ID   | Length (cm) | Width (cm) | Height (cm) | Thickness (cm) | External Volume (L) | Internal Volume (L) | Max Load (kg) | Material  | Fragile | Stackable | Waterproof | Fire Retardant | Min Temp (°C) | Max Temp (°C) | Color     | Country       |
|----------|-------------|------------|-------------|----------------|----------------------|----------------------|----------------|-----------|---------|-----------|------------|----------------|----------------|----------------|-----------|----------------|
| BX000001 | 75          | 60         | 40          | 0.4            | 180.00               | 167.78               | 350.00         | Cardboard | Yes     | Yes       | No         | No             | -30            | 60             | Brown     | Germany        |
| BX000002 | 90          | 45         | 50          | 0.2            | 202.50               | 197.28               | 450.00         | Plastic   | No      | Yes       | Yes        | Yes            | -20            | 55             | Gray      | Japan          |

> ⚠️ Data is randomly generated based on material-specific logic and physical constraints.

---

## 🚀 API-Based Picking List Service
In addition to static datasets, this project offers a FastAPI-powered service that allows users to filter and download randomized box selections based on customizable criteria like size, material, attributes (e.g., waterproof), temperature limits, and more.

📁 Location: [box_filter_api](./box_filter_api/)

🔧 Key Files:

import_excel.py – Converts Excel datasets to a SQLite database (packages.db)

main.py – Launches the FastAPI app with endpoints for downloading filtered selections as .csv or .xlsx

📚 Instructions:
See the full guide in [README_api.md](./box_filter_api/README_api.md) for setup and usage.

🧪 Test the API:
Once running, access Swagger UI at: http://127.0.0.1:8000/docs

---
🧪 Research Applications
These datasets are intended for researchers exploring the Mixed Palletizing Problem or similar logistics/optimization tasks.

Fellow researchers are encouraged to:

Use these standardized datasets for testing and benchmarking.

Share results obtained using these databases to foster reproducibility and comparison.

Cite this repository when referencing results derived from the included files.

By using common datasets, the community can ensure consistency in evaluating different algorithmic approaches.

---
## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---
## 📖 Citation

If you use this dataset in your research or software, please cite it as:

> Adamos Daios. *Box Database Generator: Static Datasets for the Mixed Palletizing Problem*. GitHub, 2025. [https://github.com/Adamos-Daios/package-db-distributions](https://github.com/Adamos-Daios/package-db-distributions)






