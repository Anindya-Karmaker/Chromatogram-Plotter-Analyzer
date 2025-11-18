# Advanced Chromatogram Analyzer

A powerful, browser-based tool for visualizing, analyzing, and exporting chromatography data directly from ÄKTA-generated files or custom CSV/Excel sheets. No installation required.

<img width="1471" height="834" alt="image" src="https://github.com/user-attachments/assets/d34a3d03-7b85-408f-a9e0-88edb459abaa" />


## 🧬 Overview

This tool was created for researchers who need a fast, private, and flexible way to analyze chromatography data without being tied to proprietary software. It runs entirely in your web browser, meaning your experimental data never leaves your computer. It's designed to be intuitive for daily lab use while providing powerful features for in-depth analysis and generating publication-ready figures.

## 🚀 Key Features

-   **Direct ÄKTA Import:** Natively parses tab-delimited `.txt` or `.csv` files exported from GE Unicorn software (tested with v7.xx).
-   **Custom Data Import:** A flexible wizard to import data from any generic CSV or Excel (`.xlsx`, `.xls`) file by mapping columns.
-   **Interactive Multi-Axis Plotting:**
    -   Visualize multiple variables on a single plot, each with its own y-axis.
    -   Full control over line color, style, and custom labels.
-   **Advanced Peak Analysis:**
    -   Visually select an integration range with draggable lines that can **snap to the nearest fraction**.
    -   Automatically calculates **Peak Area**, **Volume**, **Asymmetry Factor (As)**, and **HETP**.
    -   Calculations update in real-time as you adjust the integration range.
-   **Protein Concentration Calculator:** Uses the integrated peak area and Beer-Lambert law parameters to estimate the total protein amount in milligrams. The result is displayed directly on the main panel.
-   **Fraction Management:**
    -   Automatically imports fraction data from ÄKTA files.
    -   Manually add, edit, or remove fractions.
    -   Toggle fraction visibility on the plot, with labels displayed as annotations.
-   **Publication-Ready Exporting:**
    -   **High-Resolution PNG:** Save the plot as a PNG at **1x, 2x, or 3x resolution**.
    -   **Full Font Customization:** A dedicated panel to control the font family and size of the title, axes, and annotations.
    -   **Copy to Clipboard:** Instantly copy the plot *exactly as it appears on screen* for pasting into presentations or lab notebooks.
-   **100% Client-Side:** Your data is processed locally in your browser. Nothing is ever uploaded to a server, ensuring complete data privacy.

## ⚙️ How to Use

No installation is needed!

1.  **Visit the Live Tool:** [https://anindya-karmaker.github.io/Chromatogram-Plotter-Analyzer/](https://anindya-karmaker.github.io/Chromatogram-Plotter-Analyzer/)
2.  **Or Download:** Download the `index.html` file from this repository and open it in any modern web browser (like Chrome, Firefox, or Edge).

---

### Step-by-Step Workflow

#### 1. Import Your Data
Use the **📁 Open ÄKTA File** button for standard Unicorn exports, or the **⚙️ Custom Import** button for any other CSV or Excel file.

#### 2. Customize the Plot
Use the **📊 Plot Selection & Styling** panel to select variables and customize their appearance. Click **📊 Update Plot** to apply changes.

![Plotting Controls](https://github.com/user-attachments/assets/753c8e5c-9747-48e7-b373-7447c09fb753)

#### 3. Analyze Peaks
-   **Enter Column Parameters:** Input your column's length in millimeters.
-   **Integrate a Peak:** In the **📐 Integration & Analysis** panel, select your primary variable (usually `UV`) and use the `Start` and `End` fields to define the peak boundaries. The `Area`, `Volume`, `Asymmetry`, and `HETP` are calculated and displayed automatically.
-   **Snap to Fractions:** If fractions are visible, the Start/End values will automatically snap to the nearest fraction when you finish editing.
  
<img width="320" height="419" alt="image" src="https://github.com/user-attachments/assets/8578f07b-cf23-43c2-b371-dc6bef645c16" />


#### 4. Calculate Concentration
The **Amount (mg)** is calculated automatically in the analysis panel. To adjust parameters:
-   Click the **🧪 Calculate Concentration** button.
-   Enter your protein's Molar Extinction Coefficient, Path Length, and Molecular Weight.
-   The amount will update in real-time on both the modal and the main analysis panel.

<img width="798" height="662" alt="image" src="https://github.com/user-attachments/assets/50b66df9-57f3-49c5-8d80-3408d77dadf6" />




#### 5. Fine-Tune Appearance & Export
-   **Customize Fonts:** Click **⚙️ Font Settings** in the **💾 Export & Actions** panel to open the font editor. Change the font family and sizes for a professional, publication-ready look.
-   **Save or Copy:** Use the `Save as PNG` button to choose a resolution and download the image, or `Copy to Clipboard` to capture the plot exactly as you see it.

<img width="603" height="524" alt="image" src="https://github.com/user-attachments/assets/fee5cfee-3631-4c05-8539-5facdbb50015" />



## 🛠️ Built With

-   [Plotly.js](https://plotly.com/javascript/) - For interactive charting.
-   [PapaParse](https://www.papaparse.com/) - For robust in-browser CSV parsing.
-   [SheetJS (js-xlsx)](https://sheetjs.com/) - For reading Excel files.
-   Plain HTML, CSS, and JavaScript - No frameworks, no servers, just a single file.

## 📄 License

All rights reserved. Unauthorized copy or distribution of this application is strictly prohibited. For inquiries, please contact the [McDonald-Nandi Lab](https://mcdonald-nandi.ech.ucdavis.edu/).
