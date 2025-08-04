# Task 1 – Laying the Foundation for Analysis

## Step-by-Step Brent Oil Price Analysis Workflow

1. **Data Collection**
   - Collect historical Brent crude oil price data from trusted sources (e.g., EIA, Yahoo Finance).
   - Compile event data related to the oil market, such as geopolitical crises, OPEC+ decisions, pandemics, and economic shocks.

2. **Data Preprocessing**
   - Clean and align the datasets.
   - Standardize date formats, handle missing values, and match event timestamps to the price timeline.

3. **Exploratory Data Analysis (EDA)**
   - Use `Matplotlib` or `Seaborn` to visualize oil price trends, volatility, and seasonality.
   - Overlay key events on the time series to observe possible visual associations with price shifts.

4. **Time Series Diagnostics**
   - Perform stationarity tests such as the Augmented Dickey-Fuller (ADF) and KPSS tests.
   - Inspect rolling statistics to assess the presence of trends and structural breaks.

5. **Change Point Detection**
   - Apply change point algorithms (e.g., Binary Segmentation, PELT) using the `ruptures` Python library.
   - Analyze the detected change points in relation to known events.

6. **Interpretation and Assumption Testing**
   - Conduct scenario and sensitivity analyses to evaluate the robustness of insights under various assumptions.

7. **Communication and Reporting**
   - Share results through interactive dashboards (e.g., Streamlit), infographics, and stakeholder briefings.

---

## 1. Visualization Tools

- Use libraries like **Matplotlib** and **Seaborn** to create visualizations that highlight patterns, seasonality, and anomalies in the oil price time series.
- These tools will be particularly useful during EDA and while presenting findings visually.

## 2. Automated Data Pipelines

- Utilize **Apache Airflow** or **Prefect** to automate data fetching, preprocessing, and integration of event datasets.
- This ensures repeatability and scalability of the analysis pipeline.

---

## 3. Event Data Compilation

A CSV file named `brent_oil_events.csv` has been compiled, containing 15 major global events from 2000 to 2024. Each record includes:

| Event Name           | Type         | Start Date | Description                                        |
|----------------------|--------------|------------|----------------------------------------------------|
| Russia-Ukraine War   | Geopolitical | 2022-02-24 | Military conflict escalating oil market tensions   |
| COVID-19 Pandemic    | Health/Econ  | 2020-03-01 | Global lockdowns drastically reduced oil demand    |
| 2008 Financial Crisis| Economic     | 2008-09-15 | Global market crash causing oil price collapse     |
| OPEC+ Production Cut | OPEC Decision| 2023-04-02 | Coordinated production cuts to stabilize prices    |
| Iran Sanctions Reimposed | Geopolitical | 2018-05-08 | U.S. withdrawal from JCPOA, affecting oil exports  |

> The full dataset includes event categories, approximate dates, and brief descriptions for historical context.

---

## 4. Assumptions and Limitations

- The analysis assumes that the event start date approximates the timing of its impact on oil prices.
- It does not account for **lag effects** or **indirect consequences** of complex events.
- Events may have overlapping or cumulative impacts, complicating attribution.

### Correlation vs. Causation

> While some events may align closely with structural breaks in the oil price series, this **does not imply causation**. The analysis may show a **temporal correlation**, but proving causal impact requires additional methods like randomized experiments or advanced econometric techniques (e.g., instrumental variables, difference-in-differences, or Granger causality).

---

## 5. Communication Formats

To ensure stakeholder engagement and clarity:

- **Interactive Dashboards** using **Streamlit** or **Dash** allow users to explore change points and events.
- **Infographics** can summarize key periods of volatility or market shifts.
- **Written reports** or **executive slide decks** provide deeper insights for policy or strategy discussions.

---

## 6. Understanding the Model and Data

### Literature Review
Key concepts from change point literature emphasize:

- Structural breaks can indicate fundamental changes in economic regimes.
- Change point models are widely used in finance, climatology, and epidemiology to detect regime shifts.

Sources include:
- Killick et al. (2012) – PELT method
- Lavielle (2005) – Change in mean and variance
- Online docs for `ruptures`, `statsmodels`, and econometric resources

---

### Time Series Analysis: Trend and Stationarity

- Brent oil price data exhibits **non-stationarity** due to trends and high volatility.
- ADF and KPSS tests are applied:
  - ADF: Tests for unit roots (stationarity around a trend)
  - KPSS: Tests for trend stationarity (null hypothesis is stationarity)

> Result: Differencing or transformation (e.g., log returns) may be necessary before modeling.

---

### Purpose of Change Point Models

Change point models aim to:

- Identify **points in time** where the statistical properties (mean, variance) of a series change.
- Capture **shocks or regime shifts** in the oil market, possibly due to events like war, sanctions, or policy changes.
- Detect **volatility regimes** which can inform investment or policy decisions.

---

### Expected Outputs of Change Point Analysis

- **Change Dates**: Estimated timestamps where breaks occur.
- **Segmented Parameters**: New mean or variance values for each segment.
- **Visualizations**: Segmented time series plots for easy interpretation.

#### Limitations:
- Results depend on algorithm settings (e.g., penalty values, model assumptions).
- Sensitive to noise and may produce false positives if not carefully tuned.
- Does not attribute causality—only identifies the “when,” not the “why.”

---

## Conclusion

This foundational work sets the stage for robust, transparent, and reproducible analysis of Brent oil price trends. By combining time series modeling, event annotation, and structured reporting, the project aims to uncover patterns and insights useful for policy, strategy, and investment decisions.

---

## Next Steps

- Finalize and refine the event dataset.
- Perform change point detection and overlay findings with key events.
- Share results through dashboards and interpret structural breaks in context.
- Explore advanced modeling techniques if needed (e.g., multivariate models, causal inference).
