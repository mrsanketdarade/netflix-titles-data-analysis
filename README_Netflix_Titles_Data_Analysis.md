<div align="center">

# 🎬 Netflix Titles Data Analysis

**Exploratory Data Analysis (EDA) using Python**

![Python](https://img.shields.io/badge/Python-Data%20Analysis-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-4C72B0)

</div>

## 🖼️ Project Overview

![Netflix Titles Data Analysis infographic](images/netflix_analysis_overview.png)

This project explores the Netflix titles dataset using Python. It demonstrates a typical data analytics workflow: inspecting and cleaning data, exploring patterns, creating visualizations, and summarizing observations about the catalog.

> **Note:** The infographic is a visual overview. Verify every displayed count and insight against the exact version of `netflix_titles.csv` included with your project. Dataset versions may differ.

## 🎯 Objectives

- Understand the dataset structure and data types.
- Identify missing values and duplicates.
- Analyze Movies and TV Shows by content type.
- Explore release years, ratings, countries, and categories.
- Analyze movie duration using numeric minute values.
- Present patterns with clear visualizations.

## 🧰 Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Analysis and scripting |
| Pandas | Data cleaning and transformation |
| NumPy | Numerical operations |
| Matplotlib | Plotting and chart customization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive analysis |

## 📂 Project Structure

```text
Netflix-Titles-Data-Analysis/
├── README.md
├── netflix_titles.csv
├── Netflix_Titles_Data_Analysis.ipynb
├── Netflix_Titles_Data_Analysis.html
└── images/
    └── netflix_analysis_overview.png
```

Keep the CSV in the location expected by the notebook, or update the dataset path in the notebook.

## 🚀 Run Locally

### 1. Clone your repository

Replace the example URL with your GitHub repository URL.

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Launch the notebook

```bash
jupyter notebook Netflix_Titles_Data_Analysis.ipynb
```

Run the cells from top to bottom. Alternatively, start JupyterLab with:

```bash
jupyter lab
```

## 🔍 Analysis Workflow

1. **Load and inspect:** review dataset shape, columns, types, and summary statistics.
2. **Clean and prepare:** check missing values and duplicates, and prepare fields for analysis.
3. **Transform fields:** convert `release_year` to numeric and parse `date_added` as a datetime where needed.
4. **Explore patterns:** compare content types and examine ratings, countries, and categories.
5. **Visualize:** use charts to communicate distributions and relationships.
6. **Summarize:** document observations supported by the notebook outputs.

## 📊 Visualizations

Depending on the charts included in the notebook, the analysis may cover:

- Movie and TV Show distribution
- Release-year distribution
- Content-rating distribution
- Country and category frequency
- Movie duration versus release year
- Box plots and correlation heatmaps for selected numeric fields

For duration analysis, extract the numeric part of `duration` and use Movie records when measuring minutes. TV Show duration values usually represent seasons, not minutes.

## 🧹 Example Data Preparation

```python
df['release_year'] = pd.to_numeric(df['release_year'], errors='coerce')

df['date_added'] = pd.to_datetime(
    df['date_added'].astype('string').str.strip(),
    format='mixed',
    errors='coerce'
)
```

Handle missing text values in fields such as `director`, `cast`, `country`, and `rating` according to the analysis goal. Avoid applying numeric methods such as mean imputation to text columns.

## 💡 Questions Explored

- How does the number of Movies compare with TV Shows?
- Which release years are most represented?
- Which ratings appear most often?
- Which countries and categories appear frequently?
- What is the distribution of movie durations?
- Which fields contain missing values?

Use the notebook's actual output for the answers; counts and findings can vary by dataset version.

## 📁 Dataset

**File:** `netflix_titles.csv`

Common columns include `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, and `description`. The exact fields and row count depend on the dataset version.

## 🔮 Future Improvements

- Build an interactive dashboard using Streamlit or Plotly.
- Add filters for content type, year, rating, and country.
- Improve data-quality checks and document missing-value treatment.
- Add screenshots of actual notebook outputs.
- Extend time-based analysis where the data supports it.

## 🤝 Contributing

Suggestions are welcome. Open an issue or submit a pull request describing the proposed improvement.

## ⚠️ Disclaimer

This project is for educational and portfolio purposes. It analyzes a supplied dataset and is not affiliated with or endorsed by Netflix. It does not represent Netflix's live catalog.

---

<div align="center">

**Made with Python and curiosity 📊**

</div>
