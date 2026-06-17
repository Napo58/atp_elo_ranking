# 🎾 ATP Elo Ratings Scraper

A Python web scraper that extracts the top 100 ATP players' Elo ratings from [TennisAbstract](https://tennisabstract.com/reports/atp_elo_ratings.html) and structures them into a clean, exportable dataset.

---

## 📋 Description

This project scrapes the ATP Elo ratings table from TennisAbstract, parses it using **BeautifulSoup**, cleans the data (removing empty columns and formatting player names), and loads it into a **pandas DataFrame**. Results can be exported to a CSV file for further analysis.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook or JupyterLab

### Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/atp-elo-scraper.git
cd atp-elo-scraper
pip install requests beautifulsoup4 pandas openpyxl lxml
```

Or, from inside the Jupyter notebook:

```python
%pip install requests beautifulsoup4 pandas openpyxl lxml selenium
```

---

## 📦 Dependencies

| Library | Purpose |
|---|---|
| `requests` | Fetching the TennisAbstract page |
| `beautifulsoup4` | Parsing HTML content |
| `lxml` | HTML parser backend |
| `pandas` | Structuring and cleaning data |
| `openpyxl` | Optional Excel export support |

---

## 💻 Usage

1. Open `atp_elo_ranking.ipynb` in Jupyter Notebook or JupyterLab
2. Run all cells
3. The top 100 ATP Elo ratings will be printed as a cleaned DataFrame
4. To export to CSV, uncomment the last line:

```python
df_atp_clean.to_csv('df_atp_elo.csv', index=False)
```

---

## 🧹 Data Cleaning

The raw scraped data goes through the following cleaning steps:

- **Empty columns removed** (columns 4, 11, and 14)
- **Non-breaking spaces** (`\xa0`) stripped from column headers
- **Player names** cleaned by removing spaces and non-breaking spaces

---

## 📁 Project Structure

```
atp-elo-scraper/
│
├── atp_elo_ranking.ipynb     # Main Jupyter notebook
├── df_atp_elo.csv            # Output file (generated)
└── README.md
```

---

## 🌐 Data Source

Data sourced from [TennisAbstract – ATP Elo Ratings](https://tennisabstract.com/reports/atp_elo_ratings.html), a reference site for advanced tennis statistics and analytics.

---

## 📄 License

This project is for educational and personal use only. Please respect [TennisAbstract's](https://tennisabstract.com) terms of service when scraping their data.
