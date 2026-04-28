# 🌍 Suicide Rate Analysis (Web Scraping + EDA)

## 📌 Project Overview
Suicide is a major global public health concern. This project analyzes suicide rates across countries using publicly available data scraped from Wikipedia. The goal is to explore global patterns, identify countries with the highest and lowest suicide rates, and visualize the distribution of suicide rates worldwide.

This project demonstrates key data science skills including:
- Web scraping
- Data cleaning
- Exploratory Data Analysis (EDA)
- Data visualization
- Insight generation

---

## 🎯 Objectives
The main objectives of this project are:
- Scrape suicide rate data from Wikipedia
- Clean and preprocess the dataset
- Perform exploratory analysis on suicide rates
- Identify countries with high and low suicide rates
- Visualize distribution and outliers
- Categorize countries into suicide risk groups

---

## 🗂 Dataset Source
The dataset was scraped directly from Wikipedia:

- **Wikipedia Page:** *List of countries by suicide rate*  
  https://en.wikipedia.org/wiki/List_of_countries_by_suicide_rate

---

## ⚙️ Tools & Technologies
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **BeautifulSoup**
- **Requests**
- **lxml**

---

## 📁 Project Structure

```

Suicide-Rate-Analysis/
│
├── data/
│   ├── suicide_rates_cleaned.csv
│   ├── suicide_rates_final.csv
│
├── notebooks/
│   ├── Suicide_Rate_Analysis.ipynb
│
├── visuals/
│   ├── top10_suicide_rates.png
│   ├── distribution_plot.png
│   ├── boxplot_outliers.png
│
├── README.md
├── requirements.txt
└── LICENSE

````

---

## 🚀 Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/Suicide-Rate-Analysis.git
cd Suicide-Rate-Analysis
````

### 2️⃣ Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🧾 Web Scraping Method

The suicide rate table was scraped from Wikipedia using `pandas.read_html()`, which automatically extracts HTML tables from web pages.

Example scraping code:

```python
import pandas as pd

url = "https://en.wikipedia.org/wiki/List_of_countries_by_suicide_rate"
tables = pd.read_html(url)

df = tables[0]
df.to_csv("suicide_rates_raw.csv", index=False)
```

---

## 🧹 Data Cleaning

Cleaning steps included:

* Removing Wikipedia citation markers such as `[1]`, `[2]`
* Renaming columns for readability
* Converting numeric columns to proper data types
* Handling missing values

---

## 📊 Exploratory Data Analysis (EDA)

### Key Analysis Performed

* Summary statistics (mean, median, max, min)
* Top 10 countries by suicide rate
* Bottom 10 countries by suicide rate
* Suicide rate distribution (histogram + KDE)
* Outlier detection (boxplot)

---

## 📈 Visualizations

The project includes several visualizations such as:

### 🔹 Top 10 Countries by Suicide Rate

A bar chart showing the countries with the highest suicide rates.

### 🔹 Distribution of Suicide Rates

A histogram showing the spread and density of suicide rates.

### 🔹 Outlier Detection

A boxplot used to identify countries with unusually high suicide rates.

---

## 🧠 Risk Categorization

Countries were grouped into risk categories based on suicide rate:

* **Low Risk:** < 5 per 100,000
* **Medium Risk:** 5–15 per 100,000
* **High Risk:** > 15 per 100,000

---

## 📌 Key Insights

Some insights drawn from the analysis include:

* Suicide rates vary significantly across countries.
* A small number of countries have extremely high suicide rates (outliers).
* The distribution of suicide rates is right-skewed, indicating that most countries fall within a low-to-medium range.
* Risk categorization highlights which countries may require stronger mental health interventions.

---

## ⚠️ Limitations

* Wikipedia data may not always be updated in real-time.
* Different countries may use different reporting standards.
* The dataset may reflect underreporting in some regions.

---

## 🔮 Future Work

Potential improvements to this project:

* Compare suicide rates across age groups (if data is available)
* Build an interactive dashboard using Power BI / Tableau / Streamlit
* Perform time-series analysis using WHO or World Bank suicide datasets

---

## 🤝 Contributing

Contributions are welcome.
If you’d like to improve this project, feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## 👤 Author

**Precious Ebu**
🔗 LinkedIn: *https://www.linkedin.com/in/precious-ebu*
📧 Email: *preciousaebu@gmail.com*
🌐 Portfolio: *https://preciousebu.github.io/*

---


