# Contralateral PVI Research Calculators

Static pages for two offline calculators estimating the 1-, 3-, and 5-year risk of a first later PVI on the limb opposite the index procedure.

## Pages

- `index.html` — landing page, model summary, and research-use notice.
- `calculator_without_contralateral_wifi.html` — model that does not require contralateral-limb WIfI.
- `calculator_with_contralateral_wifi.html` — model that additionally uses contralateral-limb WIfI recorded at index PVI.

## Model summary

Each calculator implements 50 bootstrap-aggregated shallow CART regression trees per horizon. Death before contralateral PVI is treated as a competing event. Censoring is handled with inverse-probability-of-censoring weights truncated at 20. Development used a patient-level 80/20 random split stratified by observed event status.

The model that does not require contralateral WIfI was fit in 70,410 patients. The model requiring recorded contralateral WIfI stage 1–4 was fit in 40,945. Internal test AUC ranged from 0.583–0.594 and 0.587–0.605, respectively. Discrimination was modest; no temporal or external validation has been performed. SHAP values were not calculated.

## Important limitation

These are research prototypes, not clinically validated decision tools or treatment recommendations. Do not use the estimates to guide individual patient care.

The pages run locally in the browser. Form values are not transmitted. No patient-level records are included in this site package.
