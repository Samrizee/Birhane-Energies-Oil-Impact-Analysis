
# Birhan Energies: Brent Oil Price Analysis

This repository contains an end-to-end data analysis project focused on understanding Brent crude oil price fluctuations over time. The objective is to identify significant change points in the time series and relate them to major geopolitical, economic, and policy-driven events.

---

## 📊 Project Goals

- Detect **structural breaks** and **regime shifts** in Brent oil prices using change point detection techniques.
- Compile and integrate a timeline of impactful **real-world events** (e.g., OPEC decisions, wars, financial crises).
- Explore the **statistical properties** of oil prices, including trends, volatility, and stationarity.
- Communicate findings through **interactive dashboards**, **visualizations**, and **written reports**.

---

## 📁 Project Structure

```
.
├── data/                 # Raw and cleaned datasets (e.g., prices, events)
├── docs/                 # Reports, diagrams, and documentation
├── notebooks/            # Jupyter notebooks for EDA, testing, and modeling
├── src/                  # Python scripts for data processing and modeling
├── tests/                # Unit tests for core logic
└── .github/workflows/    # GitHub Actions CI/CD workflows
```

---

## ⚙️ Setup Instructions

> **Note:** Setup details will be finalized and updated as the project evolves.

### 1. Clone the repository:
```bash
git clone https://github.com/Samri-zee/brent-oil-analysis.git
cd brent-oil-analysis
```

### 2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies:
```bash
pip install -r requirements.txt
```

### 4. Run tests (optional):
```bash
pytest tests/
```

---

## 📈 Tools & Technologies

- **Python 3.9+**
- **Pandas, NumPy** – data manipulation
- **Matplotlib, Seaborn** – visualization
- **Ruptures** – change point detection
- **Statsmodels** – stationarity and time series tests
- **Streamlit / Dash** – interactive dashboards
- **GitHub Actions** – CI/CD pipelines

---

## 📌 Key Files (To Be Added)

- `brent_prices.csv`: Daily or weekly historical Brent oil prices
- `brent_oil_events.csv`: Curated event timeline with types, dates, and descriptions
- `eda.ipynb`: Exploratory analysis of oil price data
- `change_point_model.py`: Core modeling logic for detecting structural breaks

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## ✍️ Authors

- Samrawit Zerfu – Data Analyst and Digital Health Developer  
  [LinkedIn](https://www.linkedin.com/) | [GitHub](https://github.com/)

---

## 📬 Contributions

Contributions are welcome! Feel free to open issues or submit pull requests as the project develops.

---

## 🚧 Status

> This project is a **work in progress**. Setup scripts and modeling pipelines are under development and will be updated regularly.
