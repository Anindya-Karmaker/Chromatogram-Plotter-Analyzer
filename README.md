# Advanced Chromatogram Analyzer

A powerful, browser-based tool for visualizing, analyzing, and exporting chromatography data directly from ÄKTA-generated files or custom CSV/Excel sheets. No installation required.

<img width="1471" height="793" alt="image" src="https://github.com/user-attachments/assets/eed13bc4-5cc9-4c74-b3ab-65c0d88bad34" />




## 🧬 Overview

This tool was created for researchers who need a fast, private, and flexible way to analyze chromatography data without being tied to proprietary software. It runs entirely in your web browser, meaning your experimental data never leaves your computer. It's designed to be intuitive for daily lab use while providing powerful features for in-depth analysis and generating publication-ready figures.

## 🚀 Key Features

-   **Direct ÄKTA Import:** Natively parses tab-delimited `.txt` or `.csv` files from GE Unicorn software (tested with v7.xx).
-   **Custom Data Import:** A flexible wizard to import data from any generic CSV or Excel (`.xlsx`, `.xls`) file by mapping columns.
-   **Save & Load Sessions:** Save your entire analysis state—including data, annotations, and all settings—into a single `.json` file. Load a session file to resume your work exactly where you left off.
-   **Interactive Multi-Axis Plotting:**
    -   Visualize multiple variables on a single plot, each with its own y-axis.
    -   Full control over line color, thickness, style, and custom labels.
-   **Advanced Peak Analysis:**
    -   Visually select an integration range with draggable lines that can **snap to the nearest fraction**.
    -   Automatically calculates **Peak Area**, **Volume**, **Asymmetry Factor (As)**, and **HETP**.
    -   Calculations update in real-time as you adjust the integration range.
-   **Rich Annotations:**
    -   **Fraction Management:** Automatically import, manually add, edit, or remove fractions and toggle their visibility on the plot.
    -   **Label Regions:** Create colored, labeled regions (e.g., "Load", "Wash", "Elution") to clearly annotate different phases of the chromatogram. These regions are also editable and appear in the legend.
-   **Protein Concentration Calculator:** Uses the integrated peak area and Beer-Lambert law parameters to estimate the total protein amount in milligrams. The result is displayed directly on the main panel.
-   **Publication-Ready Exporting:**
    -   **High-Resolution PNG:** Save the plot as a PNG at **1x, 2x, or 3x resolution**.
    -   **Full Font Customization:** A dedicated panel to control the chart title, font family, and the size of the title, axes, and annotations.
    -   **Copy to Clipboard:** Instantly copy the plot *exactly as it appears on screen* for pasting into presentations or lab notebooks.
-   **100% Client-Side:** Your data is processed locally in your browser. Nothing is ever uploaded to a server, ensuring complete data privacy.

## ⚙️ How to Use

No installation is needed!

1.  **Visit the Live Tool:** https://anindya-karmaker.github.io/Advanced_chromatogram_analyzer/
2.  **Or Download:** Download the `index.html` file from this repository and open it in any modern web browser (like Chrome, Firefox, or Edge).

---

### Step-by-Step Workflow

#### 1. Import Your Data
Use the **📁 Open ÄKTA File** button for standard Unicorn exports. For other formats, use **⚙️ Custom Import**. To save your work for later, use **💾 Save Session**, or to resume a previous analysis, use **📂 Load Session**.

#### 2. Customize the Plot
Use the **📊 Plot Selection & Styling** panel to select variables and customize their appearance. You can also set the exact X-axis range here.

<img width="335" height="570" alt="image" src="https://github.com/user-attachments/assets/d791dac5-306e-4fcf-935e-f3df1bfca4fe" />



#### 3. Annotate the Chart
-   **Manage Fractions:** Use the **🧫 Fractions** panel to add, edit, or hide fraction markers on the plot.
-   **Label Regions:** Use the **🎨 Label Regions** panel to define and color important sections like "Wash" or "Elution". These will appear as shaded areas on the plot and in the legend.

#### 4. Analyze Peaks
-   **Enter Column Parameters:** Input your column's length in millimeters.
-   **Integrate a Peak:** In the **📐 Integration & Analysis** panel, select your primary variable (usually `UV`) and use the `Start` and `End` fields to define the peak boundaries. The `Area`, `Volume`, `Asymmetry`, and `HETP` are calculated and displayed automatically.
-   **Snap to Fractions:** If fractions are visible, the Start/End values will automatically snap to the nearest fraction when you finish editing.

<img width="328" height="427" alt="image" src="https://github.com/user-attachments/assets/171a8ef9-7245-4f61-bd58-a36cd8294d2f" />



#### 5. Calculate Concentration
The **Amount (mg)** is calculated automatically. To adjust parameters, click **🧪 Calculate Concentration**, enter your protein's specific values, and the amount will update in real-time everywhere.

<img width="801" height="666" alt="image" src="https://github.com/user-attachments/assets/02a4d8ca-4b03-4610-a774-2b26bc914fc9" />



#### 6. Fine-Tune Appearance & Export
-   **Customize Fonts:** Click **⚙️ Font and Style Settings** to open the font editor. Change the chart title, font family, and sizes for a professional, publication-ready look.
-   **Save or Copy:** Use the `Save as PNG` button to choose a resolution and download the image, or `Copy to Clipboard` to capture the plot exactly as you see it.

<img width="599" height="832" alt="image" src="https://github.com/user-attachments/assets/6f7e3500-b7a6-4489-959a-523fbc5b14b5" />



## 🛠️ Built With

-   [Plotly.js](https://plotly.com/javascript/) - For interactive charting.
-   [PapaParse](https://www.papaparse.com/) - For robust in-browser CSV parsing.
-   [SheetJS (js-xlsx)](https://sheetjs.com/) - For reading Excel files.
-   Plain HTML, CSS, and JavaScript - No frameworks, no servers, just a single file.

## 📄 License

All rights reserved. Unauthorized copy or distribution of this application is strictly prohibited. For inquiries, please contact the [McDonald-Nandi Lab](https://mcdonnanld-nandi.ech.ucdavis.edu/).
