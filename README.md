# Introduction to Artificial Intelligence Lab Tasks

4 labs, ready to run on **Google Colab**. Click a badge to open and press **Runtime > Run all**.

| Lab | Open in Colab | Notebook |
|-----|---------------|----------|
| Lab 01 — Environment Setup | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab01/Lab_01_Environment_Setup.ipynb) | `lab01/Lab_01_Environment_Setup.ipynb` |
| Lab 02 — Web Scraping and EDA | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab02/Lab_02_Web_Scraping_and_EDA.ipynb) | `lab02/Lab_02_Web_Scraping_and_EDA.ipynb` |
| Lab 03 — Text and Image Features | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab03/Lab_03_Text_and_Image_Features.ipynb) | `lab03/Lab_03_Text_and_Image_Features.ipynb` |
| Lab 04 — Simple Linear Regression | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab04/Simple_Linear_Regression.ipynb) | `lab04/Simple_Linear_Regression.ipynb` |

> Replace `manaal6` in the links above with your GitHub username if different.

## Run on Colab
1. Open a lab via its badge.
2. `Runtime > Run all` (Lab 02 installs `spacy`, `textblob`, downloads `en_core_web_sm` automatically).
3. For Lab 04, no upload needed — `Salary_dataset.csv` is in the repo next to the notebook.

## Run locally
```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
jupyter notebook
```

## Contents
- `lab01/` — environment setup, Titanic EDA
- `lab02/` — web scraping + spaCy/TextBlob features + TF-IDF (`articles_raw.csv` cached fallback)
- `lab03/` — Bag-of-Words + image grayscale/flatten
- `lab04/` — Simple Linear Regression (`Salary_dataset.csv`, `housing.csv`, `house_price_regression_dataset.csv`)

Verified: Lab 04 CSV loads (`(30, 2)`), Lab 04 path fixed from `D:/...` absolute to Colab-compatible relative loader. Labs 01–03 are stock Colab-ready (`!pip install` cells included); Lab 02 full run needs `spacy`+`en_core_web_sm` on Colab.
