::: {align="center"}
# 🎬 Netflix Titles Data Analysis

### Discovering trends, content patterns, and insights from Netflix's catalog with Python

```{=html}
<p>
```
`<img src="https://img.shields.io/badge/Python-Data%20Analysis-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Data Analysis">`{=html}
`<img src="https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">`{=html}
`<img src="https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge" alt="Matplotlib">`{=html}
`<img src="https://img.shields.io/badge/Seaborn-EDA-4C72B0?style=for-the-badge" alt="Seaborn">`{=html}
```{=html}
</p>
```
**An end-to-end exploratory data analysis project exploring movies and
TV shows available in the Netflix titles dataset.**

[📊 Explore the analysis](#-project-highlights) · [🚀 Run the
project](#-run-locally) · [📈 Visualizations](#-visualization-gallery) ·
[💡 Insights](#-key-analysis-questions)
:::

------------------------------------------------------------------------

## 📌 About the Project

What can a streaming catalog tell us about content strategy? This
project explores the Netflix titles dataset to understand its content
mix, release-year patterns, ratings, genres, and other catalog
characteristics.

The workflow covers data inspection, cleaning, exploratory data analysis
(EDA), and visual storytelling using Python. It is designed as a
portfolio project to demonstrate practical data analytics skills.

> **Dataset note:** This project analyzes the supplied
> `netflix_titles.csv` file. The results describe that dataset and
> should not be interpreted as a live view of Netflix's current catalog.

## ✨ Project Highlights

  -----------------------------------------------------------------------
  🔎 Area                             What it covers
  ----------------------------------- -----------------------------------
  🧹 Data preparation                 Inspecting data types, missing
                                      values, duplicates, and
                                      inconsistent values

  📅 Date and year analysis           Exploring release years and
                                      date-added patterns

  🎞️ Content mix                      Comparing Movies and TV Shows

  🎭 Catalog exploration              Reviewing ratings, countries,
                                      directors, cast, and listed-in
                                      categories where available

  📊 Data visualization               Using plots to make trends and
                                      distributions easier to understand

  🧠 Insight generation               Turning exploratory findings into
                                      clear observations
  -----------------------------------------------------------------------

## 🧰 Tech Stack

-   **Python** --- analysis and scripting
-   **Pandas** --- data manipulation and cleaning
-   **NumPy** --- numerical operations
-   **Matplotlib** --- plotting
-   **Seaborn** --- statistical visualization
-   **Jupyter Notebook** --- interactive analysis and documentation

## 🗂️ Project Structure

``` text
Netflix-Titles-Data-Analysis/
├── netflix_titles.csv
├── Netflix_Titles_Data_Analysis.ipynb
├── Netflix_Titles_Data_Analysis.html
└── README.md
```

*Your local filenames may differ. Keep the CSV in the same folder as the
notebook, or update the dataset path in the notebook.*

## 🚀 Run Locally

### 1. Clone your repository

``` bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace the placeholder URL with your GitHub repository URL.

### 2. Install the dependencies

``` bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Add the dataset

Make sure `netflix_titles.csv` is available in the project folder.

### 4. Launch the notebook

``` bash
jupyter notebook Netflix_Titles_Data_Analysis.ipynb
```

Open the notebook and run the cells from top to bottom.

### ▶️ Prefer JupyterLab?

``` bash
jupyter lab
```

## 📈 Visualization Gallery

The notebook contains visual analysis of the Netflix catalog. Examples
of useful views include:

```{=html}
<details>
```
```{=html}
<summary>
```
`<b>`{=html}🎬 Movies vs. TV Shows`</b>`{=html}
```{=html}
</summary>
```
Compare the number of titles by content type to understand the catalog
mix.

```{=html}
</details>
```
```{=html}
<details>
```
```{=html}
<summary>
```
`<b>`{=html}📅 Titles by Release Year`</b>`{=html}
```{=html}
</summary>
```
Explore how the release years of titles are distributed and how the
catalog spans different periods.

```{=html}
</details>
```
```{=html}
<details>
```
```{=html}
<summary>
```
`<b>`{=html}⭐ Ratings Distribution`</b>`{=html}
```{=html}
</summary>
```
Review the distribution of content ratings and identify common rating
categories.

```{=html}
</details>
```
```{=html}
<details>
```
```{=html}
<summary>
```
`<b>`{=html}🌎 Countries and Categories`</b>`{=html}
```{=html}
</summary>
```
Explore country and genre/category fields to understand the catalog's
geographic and content variety.

```{=html}
</details>
```
```{=html}
<details>
```
```{=html}
<summary>
```
`<b>`{=html}⏱️ Movie Duration vs. Release Year`</b>`{=html}
```{=html}
</summary>
```
For movie records, compare release year with numeric duration after
extracting the minute value from the duration field.

```{=html}
</details>
```
> **Tip:** For a more visual GitHub README, add screenshots of your
> actual notebook charts in an `images/` folder and link them here.

## 💡 Key Analysis Questions

Use the notebook to explore questions such as:

-   What is the balance between Movies and TV Shows?
-   Which release years appear most frequently in the dataset?
-   Which content ratings occur most often?
-   Which countries and categories appear frequently?
-   How are movie durations distributed?
-   Are there missing values in important descriptive fields, and how
    should they be handled?

## 🧼 Data Preparation Notes

The analysis may require handling blank or missing values in descriptive
columns, converting `release_year` to a numeric type, and parsing
`date_added` into a consistent datetime format. Movie duration can be
converted to a numeric minute value for duration-specific analysis.

Example preprocessing patterns:

``` python
df['release_year'] = pd.to_numeric(df['release_year'], errors='coerce')

df['date_added'] = pd.to_datetime(
    df['date_added'].astype('string').str.strip(),
    format='mixed',
    errors='coerce'
)
```

Apply these steps only where they match the columns and structure in
your copy of the dataset.

## 📂 Dataset

The project uses **`netflix_titles.csv`**, containing title-level
information such as content type, title, director, cast, country, date
added, release year, rating, duration, and listed-in categories,
depending on the dataset version.

If you redistribute the dataset, follow the source's terms and
attribution requirements. This project is an independent analysis and is
not affiliated with or endorsed by Netflix.

## 🎯 Skills Demonstrated

`Python` · `Pandas` · `NumPy` · `Data Cleaning` ·
`Exploratory Data Analysis` · `Data Visualization` · `Jupyter Notebook`
· `Analytical Thinking`

## 🔮 Possible Future Improvements

-   Add an interactive dashboard with Plotly or Streamlit
-   Compare content trends across selected years
-   Create country and category filters
-   Add more robust data-quality checks
-   Publish the charts in a small web dashboard

## 🤝 Contributing

Suggestions and improvements are welcome. You can open an issue or
submit a pull request with a clear explanation of the proposed change.

## 📜 Disclaimer

This project is for educational and portfolio purposes. Findings depend
on the supplied dataset and do not represent real-time Netflix
availability or recommendations.

------------------------------------------------------------------------

::: {align="center"}
**⭐ If you find this project useful, consider giving the repository a
star!**

Made with 🐍 Python and 📊 curiosity.
:::
