# 🩺 Medical Data Visualizer

---

## 📊 Project Overview

- **Dataset**: `medical_examination.csv`
- **Tech Stack**: Python, pandas, seaborn, matplotlib
- **Key Visualizations**:
  - 📈 Categorical Plot
  - 🔥 Heatmap of Correlation Matrix

---

## 🏥 Features Visualized

- `cholesterol`, `gluc`, `alco`, `active`, `smoke`, `overweight`
- Plotted against cardiovascular disease indicator (`cardio`)

---

## 🧪 Data Processing Steps

1. **BMI Calculation**: Added an `overweight` column by calculating BMI (`weight / height²`) and classifying as overweight if BMI > 25.
2. **Normalization**: Re-coded cholesterol and glucose values to simplify analysis (1 → 0, 2 or 3 → 1).
3. **Filtering** (for heatmap):
   - Removed rows with inconsistent blood pressure (`ap_lo > ap_hi`)
   - Removed outliers based on height and weight (outside 2.5th and 97.5th percentiles)

---

## 📉 Categorical Plot

Shows the distribution of binary lifestyle indicators and health factors for patients with and without cardiovascular disease.

### 🖼️ Output:

![Categorical Plot](catplot.png)

---

## 🔥 Heatmap

Shows correlations between various medical features.

### 🖼️ Output:

![Heatmap](heatmap.png)

---

## 🧪 Testing

Unit tests (`test_module.py`) validate:
- Correct labels and structure of categorical plot
- Accuracy of values and labels in the heatmap

Run tests with:

```bash
python main.py
