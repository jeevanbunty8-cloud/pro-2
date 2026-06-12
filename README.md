
```markdown
# Scotch Whisky Flavor Profile Analysis and Geolocation Mapping

This project performs Exploratory Data Analysis (EDA) on a collection of Scotch whisky distilleries. It uncovers relationships between sensory flavor characteristics (such as smokiness, sweetness, and medicinal attributes) and maps their corresponding geographic coordinates (Latitude and Longitude) within Scotland.

---

## Table of Contents
1. [Dataset Overview](#dataset-overview)
2. [Project Structure](#project-structure)
3. [Installation & Requirements](#installation--requirements)
4. [Key Steps & Features](#key-steps--features)
5. [Visualizations](#visualizations)
6. [How to Run](#how-to-run)

---

## Dataset Overview

The project utilizes a dataset named `whisky.csv` containing profiles for **86 distilleries** across **17 specific attributes**:
* **Categorical / Identifier Columns:** `RowID`, `Distillery`, `Postcode`.
* **Flavor Profile Attributes (Scored 0–4):** `Body`, `Sweetness`, `Smoky`, `Medicinal`, `Tobacco`, `Honey`, `Spicy`, `Winey`, `Nutty`, `Malty`, `Fruity`, `Floral`.
* **Geospatial Coordinates:** `Latitude`, `Longitude`.

---

## Project Structure

```text
├── whisky.csv          # Main whiskey distillery profiling dataset
├── code.ipynb          # Jupyter Notebook containing analysis and visualizations
└── README.md           # Project documentation (this file)

```

---

## Installation & Requirements

Ensure you have a Python environment (v3.8+) configured. You can install the required data science libraries via pip:

```bash
pip install pandas numpy matplotlib seaborn jupyter

```

---

## Key Steps & Features

### 1. Data Ingestion & Integrity Checks

* Loads the dataset with `pandas`.
* Examines structural shapes, sizes, dimensions (`86 rows x 17 columns`), and explicit data types.
* Inspects missing entries via `.isnull().sum()` to confirm data completeness.

### 2. Statistical Profiling

* Generates descriptive statistics summary charts using `.describe()` to isolate behavior means, variance bounds, and quantile distribution spans.

### 3. Correlation Analysis

* Calculates a correlation matrix mapping linear relationships between independent tasting dimensions and spatial attributes.
* *Insights discovered:* For example, a strong positive correlation is observed between `Smoky` and `Medicinal` properties (~0.68), while a negative relationship appears between `Medicinal` profiles and geographical `Latitude` coordinates (~ -0.67).

---

## Visualizations

The notebook utilizes `matplotlib` and `seaborn` to output analytical plots, including:

* **Flavor Component Correlation Matrix:** A visual breakdown of how distinct sensory features tie together or oppose one another.
* **Geospatial Path Mapping:** A line visualization tracking directional coordinates (`Longitude` vs. `Latitude`) mapping distillery chains or geographical distributions across regional boundaries.

---

## How to Run

1. Clone or download this project repository locally.
2. Ensure `whisky.csv` is placed in the exact same directory as your script.
3. Start up the notebook platform from your terminal terminal:
```bash
jupyter notebook code.ipynb

```


4. Run all code blocks sequentially to verify metrics and generate plot components.

```

```
