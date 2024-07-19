## Bartemes et al. MxIMC Spatial Analysis

Hyperion multiplex IMC analysis notebooks and example data for Bartemes et al. *Increased interaction between B cells and CD3+ T cells is a hallmark of non-progression in human papilloma virus-associated oropharyngeal squamous cell carcinoma*

---

### Scripts

**01-xgboost_classification.ipynb**
- Input: Individual ROI cell marker quantification tables with cell-type annotations (exported from QuPath) for each image.
- Performs Box Cox normalization of marker signal.
- Trains XGBoost classifier for cell type prediction.
- *Outputs of this notebook must be loaded back into QuPath for nearest neighbor calculations between cell types.*

**02-prep_allClassData.ipynb**
- Input: Individual ROI quantification files including nearest cell-type neighbors.
- Merges quantification files from all images into a single data frame for input into spatial analyses.

**03-spatial_analysis.ipynb**
- Input: Merged quantification table.
- Performs spatial analysis, including spatial interaction and pairwise distance associations.

**04-niche_analysis.ipynb**
- Input: Merged quantification table.
- Performs niche analysis, identifying nine spatially-associated cell niches via k-means clustering.

**05-niche_survival.Rmd**
- Performs survival analysis, testing patient outcomes with respect to niche composition of corresponding ROIs.
- *Requires survival data, full dataset available upon request.*

---

### Data
Sample data from four ROIs is provided in example_quant_HPV_OPSCC.zip. One thousand rows of marker quantification data for each ROI is provided, including cell annotations. Full Hyperion dataset is available upon request to the authors.

---
### Contact
First author: [Kathleen Bartemes, Ph.D.](mailto:Bartemes.Kathleen@mayo.edu)
Corresponding author: [Kathryn M. Van Abel, M.D.](mailto:VanAbel.Kathryn@mayo.edu)

Bioinformatic analyses performed by [Brenna Novotny, M.S.](mailto:Novotny.Brenna@mayo.edu) and [Raymond Moore, M.S.](mailto:Moore.Raymond@mayo.edu)
