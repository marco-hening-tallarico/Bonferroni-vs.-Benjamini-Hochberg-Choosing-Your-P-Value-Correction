# Bonferroni vs. Benjamini–Hochberg: Choosing Your P-Value Correction

## Overview
This repository contains an interactive Jupyter Notebook that explores two common multiple-testing correction methods — the Bonferroni correction and the Benjamini–Hochberg (BH) procedure — and shows when each approach is appropriate. It provides intuition, examples, visualizations, and runnable code to compare family-wise error control (Bonferroni) vs. false discovery rate control (BH).

## Contents
- `Bonferroni_vs_BH.ipynb` — Main Jupyter Notebook with:
  - conceptual explanation of both corrections
  - simulated examples comparing Type I/II error tradeoffs
  - visualizations of adjusted p-values and discoveries
  - guidance on choosing a correction for different analysis goals

(If your notebook filename differs, rename the reference above or update the file.)

## Background / Motivation
When performing multiple hypothesis tests, using raw p-values leads to inflated error rates. Two commonly used approaches:
- Bonferroni correction: controls the family-wise error rate (FWER) by making the test more conservative (reduces false positives at the cost of power).
- Benjamini–Hochberg (BH) procedure: controls the false discovery rate (FDR), allowing more discoveries while controlling the expected proportion of false discoveries.

This notebook demonstrates the practical differences and helps users choose an appropriate correction depending on the scientific question and tolerance for false positives.

## Requirements
This repository was developed using a typical scientific Python stack. Suggested environment:
- Python 3.8+
- Jupyter (Notebook or Lab)
- numpy
- pandas
- scipy
- statsmodels (for `multipletests`)
- matplotlib / seaborn

You can install common dependencies with:
```bash
python -m venv venv
source venv/bin/activate    # or `.\venv\Scripts\activate` on Windows
pip install --upgrade pip
pip install jupyter numpy pandas scipy statsmodels matplotlib seaborn
```
Or create a `requirements.txt` and run:
```bash
pip install -r requirements.txt
```

## How to run
1. Clone the repository:
   ```bash
   git clone https://github.com/marco-hening-tallarico/Bonferroni-vs.-Benjamini-Hochberg-Choosing-Your-P-Value-Correction.git
   cd Bonferroni-vs.-Benjamini-Hochberg-Choosing-Your-P-Value-Correction
   ```

2. Start Jupyter and open the notebook:
   ```bash
   jupyter notebook Bonferroni_vs_BH.ipynb
   ```
   or start Jupyter Lab:
   ```bash
   jupyter lab
   ```

3. (Optional) Open directly in Google Colab:
   - Use the Colab open URL pattern:
     `https://colab.research.google.com/github/<owner>/<repo>/blob/main/<notebook>.ipynb`
   - Example:
     `https://colab.research.google.com/github/marco-hening-tallarico/Bonferroni-vs.-Benjamini-Hochberg-Choosing-Your-P-Value-Correction/blob/main/Bonferroni_vs_BH.ipynb`
   - Replace `<notebook>.ipynb` with the actual notebook name if different.

## What you'll learn
- How Bonferroni and BH adjust p-values or thresholds
- Practical consequences for Type I error, power, and the number of discoveries
- Example workflows for exploratory vs. confirmatory analyses
- How to implement corrections using Python (`statsmodels.stats.multitest.multipletests`)

## References
- Benjamini, Y. & Hochberg, Y. (1995). Controlling the False Discovery Rate: A Practical and Powerful Approach to Multiple Testing. Journal of the Royal Statistical Society B.
- Standard statistics texts and statsmodels documentation for `multipletests`.

## Contributing
Contributions, suggestions, and bug reports are welcome. If you add new notebooks, data, or examples, please:
- Open an issue describing the change
- Submit a pull request with a clear description of the addition

## License
If you intend this work to be shared under a specific license, add a `LICENSE` file in the repository. If none is present, consider adding an open license (e.g., MIT, CC BY) so others know how they may reuse the material.

## Contact
Maintainer: Marco Hening Tallarico — (GitHub: [marco-hening-tallarico](https://github.com/marco-hening-tallarico))

---
If you’d like, I can:
- adjust the README to reference the exact notebook filename(s) in the repo,
- add a requirements.txt based on the notebook's imports,
- or generate a short usage demo (GIF or static images) for the README.
```
