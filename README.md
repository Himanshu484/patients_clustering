
# Topological Data Analysis of the WISE Study

A novel approach to patient stratification and mortality prediction using Topological Data Analysis (TDA) for women with suspected ischemic heart disease.

## Overview

This repository contains the implementation of a groundbreaking study that applies Topological Data Analysis to the Women's Ischemia Syndrome Evaluation (WISE) study dataset [1]. Our research demonstrates how TDA can effectively segregate women into distinct patient subsets with significantly different long-term mortality risks, representing a paradigm shift toward precision medicine in cardiovascular care.

## Research Background

Traditional risk stratification methods in cardiovascular medicine often rely on linear models that may fail to capture complex, multidimensional relationships in clinical data [1]. This study harnesses the power of TDA to identify distinct patient subsets and evaluate their association with long-term mortality outcomes [1].

### Key Findings
- **Two Distinct Clusters**: TDA successfully identified two patient clusters with markedly different clinical profiles [1]
- **Cluster A (n=386)**: Higher mortality risk, characterized by previous cardiovascular interventions and specific medication profiles [1]
- **Cluster B (n=433)**: Lower mortality risk, featuring more comorbid conditions and medical complexity [1]
- **Significant Survival Differences**: Kaplan-Meier analysis revealed striking long-term mortality differences between clusters [1]

## Getting Started

### Prerequisites

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
pip install kmapper umap-learn lifelines scipy
pip install sas7bdat openpyxl
```

### Data Structure

```
├── Data/
│   ├── wise1compdata10212019(1).sas7bdat    # Original WISE dataset
│   ├── Variables.xlsx                        # Selected variables list
│   ├── up_cluster.csv                       # Cluster A patient indices
│   ├── down_cluster.csv                     # Cluster B patient indices
│   └── processed/                           # Generated processed datasets
├── analysis.py                              # Main analysis script
└── README.md
```

## Usage

Run the complete analysis pipeline:

```python
python analysis.py
```

### Key Analysis Steps

1. **Data Preprocessing**: Load and clean 132 clinical variables
2. **Topological Analysis**: Apply Mapper algorithm with UMAP projection
3. **Cluster Identification**: Extract two distinct patient populations
4. **Survival Analysis**: Generate Kaplan-Meier curves
5. **Statistical Testing**: Perform comparative analysis between clusters

### Generated Outputs

- `WISE_keplermapper_output.html` - Interactive topological network visualization
- `kaplan_meier_plot.png` - Survival curve comparison (300 DPI)
- Processed datasets in CSV format
- Statistical summaries and t-test results

## 🔍 Methodology

### Topological Data Analysis
- **Algorithm**: Sophisticated Mapper algorithm implementation
- **Projection**: UMAP dimensionality reduction (2-3 components)
- **Clustering**: DBSCAN with optimized parameters
- **Visualization**: Interactive network graphs revealing patient similarity patterns

### Statistical Analysis
- Kaplan-Meier survival analysis for 10-year mortality assessment
- Log-rank tests for statistical significance evaluation
- Comprehensive cluster characterization and comparison

## Results

The analysis reveals two clinically distinct patient phenotypes:

**Cluster A Characteristics** [1]:
- Previous cardiovascular interventions
- Nitrate usage, tamoxifen therapy
- Prior PTCA and MI history
- Elevated estradiol levels
- **Higher long-term mortality risk**

**Cluster B Characteristics**:
- Congestive heart failure history
- Digitalis and corticosteroid therapy
- Significant renal dysfunction
- Peripheral vascular disease
- **Lower long-term mortality risk**

## Clinical Implications

This innovative methodology represents a paradigm shift toward precision medicine in cardiovascular care, potentially transforming how we identify high-risk patients and tailor therapeutic interventions. The TDA-identified clusters provide clinically actionable insights for treatment decisions and risk management strategies.

## Author

- **Himanshu Yadav, MS** - Department of Mathematics, University of Florida  


## Contact

For questions regarding this research or code implementation:
- Himanshu Yadav: yadav.himanshu@ufl.edu
- University of Florida, Department of Mathematics

## Important Note

This analysis uses clinical data from the WISE study. Ensure proper IRB approval and data use agreements are in place before using this code with any clinical datasets.

---
