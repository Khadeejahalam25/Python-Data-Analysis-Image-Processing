# Python Data Analysis & Image Processing

A set of three Python mini-projects covering procedural programming, image processing with NumPy, and data wrangling with Pandas.

## Contents

### 1. Frozen Yogurt & Ice Cream Order System
An interactive command-line ordering system that:
- Takes customer orders (product type, size, container, toppings, add-ons)
- Calculates order totals with a weekend discount rule
- Tracks returning customers
- Generates a final sales report — total orders, total sales, and average order value per item

### 2. Image Color Transformation (NumPy + PIL)
Takes a black-and-white checkered pattern image and reprograms its colors using NumPy array manipulation — remapping pixel values directly rather than using built-in filters, to demonstrate array-level image processing.

### 3. Timetable Parser (Pandas)
Parses a real, messily-formatted university timetable spreadsheet (`.xlsx`) — which has a multi-row header block combining a title, a degree-program legend, and merged time-slot columns — into a clean, tidy `pandas` DataFrame with the columns:

| index | day | room | time | course | type |
|---|---|---|---|---|---|

The parser dynamically detects time-slot columns and room rows rather than hardcoding cell positions, so it adapts if rows are added/removed, and uses a relative file path so it runs on any machine after cloning the repo.

## Tech Stack

- **Language:** Python 3
- **Libraries:** `pandas`, `numpy`, `Pillow (PIL)`, `matplotlib`, `openpyxl`
- **Environment:** Jupyter Notebook

## Project Structure

```
Python-Data-Analysis-Image-Processing/
├── data_processing_toolkit.ipynb    # Main notebook — all 3 mini-projects
├── test.jpg                         # Sample image used for image processing
├── timetable-fsc-fall-2023.xlsx     # Sample timetable used for the parser
└── README.md
```

## Running it

```bash
git clone https://github.com/<your-username>/Python-Data-Analysis-Image-Processing.git
cd Python-Data-Analysis-Image-Processing
pip install pandas numpy pillow matplotlib openpyxl
jupyter notebook data_processing_toolkit.ipynb
```

The order system is interactive and expects console input when run cell-by-cell in Jupyter. The image processing and timetable parsing sections run end-to-end with no input required.

## Timetable Parser — Notes

The raw timetable file has a non-trivial layout: the first several rows contain a title and a degree-program legend, and the actual per-room schedule starts a few rows down with each time slot spanning multiple merged spreadsheet columns. The notebook parses this structure programmatically (detecting the header row and time-slot boundaries) rather than assuming fixed cell coordinates, so the same logic can be pointed at other sheets (Tuesday/Wednesday/Thursday) with minimal changes.

## Author

Khadeejah — Data Science Student, FAST NUCES Islamabad
