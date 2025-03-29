# Enhancing Modelling Approaches for Analysing *Chalinolobus gouldii* Vocalisation Behaviour  
**STAT3926/STAT4026: Statistical Consulting Project**  
📅 **Published:** May 20, 2024  
👨‍💻 **Authors:** 520432255, 500480816, 500573428  
🎯 **Client:** Magic Mei-Ting Kao

---

## 📌 Project Summary

This consulting project focused on evaluating and enhancing the client’s current statistical modelling workflow for analysing the vocalisation behaviour of *Chalinolobus gouldii* (Gould’s wattled bats). We confirmed that a Poisson Generalised Linear Mixed Model (GLMM) is appropriate, implemented enhancements, validated assumptions, and recommended a reproducible and adaptable framework to support the client’s PhD thesis.

---

## 🎯 Client’s Aims

- Determine **factors affecting vocalisation activity** at foraging sites.
- Evaluate the suitability of existing models and implement **GLMMs** with nested random effects.
- Provide a **reproducible workflow** for analysing general activity and social call activity.

---

## 🧠 Methodology

### 📊 Data Overview

- Bat activity and environmental covariates collected across **multiple sites and dates**.
- Variables include bat activity counts, vegetation, temperature, rainfall, and anthropogenic factors.
- Focused on three **key reproductive periods**: mating, breeding, and pregnancy.

### 🛠 Modelling Workflow

1. Data preprocessing and filtering.
2. **EDA**: Histograms, skewness checks, correlation matrix.
3. Model fitted: **Poisson GLMM**, with date nested within location.
4. Diagnostics via **DHARMa**: residuals, dispersion, outlier and zero-inflation tests.
5. Visualised fixed and random effects to interpret ecological relevance.

---

## 🔍 Key Insights

- 🦇 **Activity is significantly lower** during mating (67%) and pregnancy (65%).
- 🌡️ Each 1°C rise in temperature increases activity by **9%** (*p* < 0.01).
- 🏙️ Anthropogenic features significantly reduce activity by **27%** (*p* < 0.05).
- 🌧️ Rainfall and water areas had **non-significant effects**.
- 📍 Random effects showed major location-specific variability:
  - High activity at **BLH_w4** (+62%) and **SOP_brickpit** (+34%).
  - Low activity at **CTNP_duck** (22%) and **CSF_w** (71%).

---

## ✅ Model Diagnostics

| Diagnostic Test          | Result                  |
|--------------------------|-------------------------|
| Kolmogorov-Smirnov       | p = 0.156 ✅             |
| Dispersion               | p = 0.216 ✅             |
| Outlier Detection        | p = 0.9 ✅               |
| Zero-Inflation           | p = 0.97 ✅ (well-fit)   |

These results confirm the **Poisson GLMM** as a robust model for the data.

---

## 📈 Visual Outputs

- **Figure 1**: Correlation heatmap  
- **Figure 2**: Distribution of `overall_activity`  
- **Figure 12**: Residual diagnostic plots  
- **Figure 13**: Fixed effects estimates with significance indicators  
- **Figure 14**: Random effects per location visualisation

---

## 🧭 Recommendations

- Continue using **Poisson GLMM**, enhanced with:
  - Robust residual checks
  - Clear fixed/random effects interpretation
- Apply same workflow to **social call activity analysis**
- Validate models in `brms` and `MCMCglmm` for publication-ready analysis
- Maintain focus on **reproducibility** and **scientific rigour**

---
