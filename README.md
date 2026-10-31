# RZ-USFM: Radiomics-Regularized Ultrasound Foundation Model with Bayesian Fusion for Breast Biopsy Triage

Code for the paper by Haddadi, Hazarika, Djabou and Alsolai (2026, under review).

Three experts (radiomics, dual-stream ConvNeXt, and **RZ-USFM**, a USFM foundation model regularised with radiomic concepts) are combined by a hierarchical Bayesian fusion, followed by conformal biopsy triage with guaranteed sensitivity.

## Notebooks (run in order on Google Colab, GPU)

1. `Part1_Radiomics_ExpertA.ipynb` – radiomics, ICC stability, concepts, Expert A
2. `Part2_Deep_ExpertB.ipynb` – dual-stream deep expert
3. `Part3_RZUSFM_ExpertC.ipynb` – RZ-USFM and consistency score
4. `Part4_Fusion_Triage.ipynb` – Bayesian fusion and conformal triage
5. `Part5_External_BUSI.ipynb` – external validation on BUSI

## Data and weights (not included)

- BUS-BRA: [doi:10.1002/mp.16812](https://doi.org/10.1002/mp.16812)
- BUSI: [doi:10.1016/j.dib.2019.104863](https://doi.org/10.1016/j.dib.2019.104863)
- USFM weights: [openmedlab/USFM](https://github.com/openmedlab/USFM)

Set the Drive paths in the first cell of each notebook.

## Results

AUC 0.951 internally (BUS-BRA) and 0.973 externally (BUSI); at α = 2%, 24.3% of benign BI-RADS 4 biopsies avoided (sensitivity 98.8%).

## License

Non-commercial research use (USFM is CC BY-NC 4.0).
