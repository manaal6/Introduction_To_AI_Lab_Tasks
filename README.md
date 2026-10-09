# Introduction to Artificial Intelligence Lab Tasks

6 labs. Labs 01–05 run on **Google Colab** — click a badge and press **Runtime > Run all**.

> Lab 06 is a deployment lab (FastAPI + dashboard) — it runs locally, see `lab06/` below.

| Lab | Open in Colab | Notebook |
|-----|---------------|----------|
| Lab 01 — Environment Setup | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab01/Lab_01_Environment_Setup.ipynb) | `lab01/Lab_01_Environment_Setup.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab01/Lab_01_Environment_Setup.ipynb) · `lab01/Lab_01_Environment_Setup.pdf` |
| Lab 02 — Web Scraping and EDA | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab02/Lab_02_Web_Scraping_and_EDA.ipynb) | `lab02/Lab_02_Web_Scraping_and_EDA.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab02/Lab_02_Web_Scraping_and_EDA.ipynb) · `lab02/Lab_02_Web_Scraping_and_EDA.pdf` |
| Lab 03 — Text and Image Features | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab03/Lab_03_Text_and_Image_Features.ipynb) | `lab03/Lab_03_Text_and_Image_Features.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab03/Lab_03_Text_and_Image_Features.ipynb) · `lab03/Lab_03_Text_and_Image_Features.pdf` |
| Lab 04 — Simple Linear Regression | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab04/Simple_Linear_Regression.ipynb) | `lab04/Simple_Linear_Regression.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab04/Simple_Linear_Regression.ipynb) · `lab04/Simple_Linear_Regression.pdf` |
| Lab 05 — Diabetes & Logistic Regression | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab05/Lab_05_Diabetes_Logistic_Regression.ipynb) | `lab05/Lab_05_Diabetes_Logistic_Regression.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab05/Lab_05_Diabetes_Logistic_Regression.ipynb) · `lab05/Lab_05_Diabetes_Logistic_Regression.pdf` |
| Lab 06 — Diabetes Dashboard (FastAPI) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab06/Lab_06_Diabetes_Deployment.ipynb) | `lab06/Lab_06_Diabetes_Deployment.ipynb` | [Colab link](https://colab.research.google.com/github/manaal6/Introduction_To_AI_Lab_Tasks/blob/main/lab06/Lab_06_Diabetes_Deployment.ipynb) · `lab06/Lab_06_Diabetes_Deployment.pdf` — app runs locally, see below |

> The `labXX/*.pdf` files are the executed notebooks exported **with outputs** (see "PDFs with outputs" below).

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
- `lab05/` — Diabetes exploration + Logistic Regression (`diabetes.csv`)
- `lab06/` — Diabetes prediction dashboard: sir's FastAPI backend (`main.py`) + frontend (`index.html`).
  Run locally: `cd lab06 && python -m uvicorn main:app --port 8000`, then open `index.html` in the browser
  (it calls `http://localhost:8000/predict`). API docs at `http://localhost:8000/docs`.

## PDFs with outputs

Each `labXX/*.pdf` is the lab's notebook after **Runtime > Run all on Colab**, exported via **File > Print > Save as PDF** so all cell outputs (tables, plots) are visible.

To regenerate a PDF: open its Colab link above → `Runtime > Run all` → `File > Print` → `Save as PDF` → place it next to the notebook (`lab01/`, `lab02`, …).

Verified: Lab 04 CSV loads (`(30, 2)`), Lab 04 path fixed from `D:/...` absolute to Colab-compatible relative loader. Labs 01–03 are stock Colab-ready (`!pip install` cells included); Lab 02 full run needs `spacy`+`en_core_web_sm` on Colab.
