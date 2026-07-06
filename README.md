# Stratifying Depression Subtypes via Systemic Inflammation

## 🎯 Clinical & Business Problem
* **The Challenge:** Over 30% of patients with Major Depressive Disorder do not respond to standard SSRI antidepressants because depression is treated as a single, identical condition.
* **The Solution:** Clinical research suggests a distinct biological subtype exists: **Inflammatory Depression**. 
* **The Goal:** This project uses healthcare analytics on NHANES data to separate depressed cohorts into biological biotypes (high vs. low inflammation) and identifies the unique behavioral and socioeconomic patterns that define them.

---

## 🛠️ AI-Augmented Workflow
Modern analytics relies on pairing human domain expertise with AI efficiency. This project utilized an intentional, co-piloted workflow:

* **Data Troubleshooting:** When the initial dataset was missing the vital C-Reactive Protein (CRP) biomarker, an AI assistant provided an automated fallback script using `pd.read_sas()` to stream the raw CDC/NHANES transport files directly.
* **Schema Mapping:** AI was used to quickly parse opaque NHANES codebooks (e.g., mapping categorical `1` and `2` values, and clearing `7` and `9` missing/refused data flags).
* **Data Visualization:** Moving past basic bar charts, the workflow leveraged AI feedback to build advanced **violin plots** and **stratified percentage distributions** to show the true population density and data skewness.

---

## 📋 Key Findings

By applying strict clinical thresholds (PHQ-9 score >= 10 for depression; High-Sensitivity CRP > 3.0 mg/L for high inflammation), the dataset was split into two balanced cohorts: **199 Inflammatory** patients and **228 Non-Inflammatory** patients.

While subjective symptoms like sleep duration and sleep quality were completely identical between both groups, major lifestyle and economic differences emerged:

* **Socioeconomic Stress:** The Inflammatory group presented with a lower Income-to-Poverty Ratio (1.74 vs. 1.84), pointing to financial strain as a chronic driver of systemic physiological inflammation.
* **Physical Health Perception:** Patients with high inflammation reported worse self-perceived general health (3.69 vs. 3.52 on a scale where 5 is poor). 
* **Substance Use Skew:** Violin plot analysis revealed that while the median alcohol intake was identical (2.0 drinks/day), the Inflammatory cohort contained a heavy concentration of severe drinking outliers—highlighting alcohol consumption as a direct mechanical trigger for high CRP.

---

## 🚀 Recommendations

1. **Incorporate Blood Panels:** Psychiatric intake processes should combine traditional behavioral questionnaires (PHQ-9) with baseline blood work (hs-CRP) to immediately flag the inflammatory subtype.
2. **Targeted Treatment Paths:** Because the inflammatory cohort is heavily impacted by alcohol usage and socioeconomic stress, their treatment plans should prioritize integrated lifestyle counseling alongside standard care.
3. **Clinical Trial Stratification:** Pharmaceutical teams should specifically isolate patients meeting these exact criteria (PHQ-9 >= 10, CRP > 3.0) when testing anti-inflammatory agents as secondary treatments for depression.
