# Electricity Consumption Trend Analysis

An exploratory time-series analysis of electricity usage, monthly operating
hours, tariff rates, and electricity bills using Python. The notebook combines
rolling averages with linear trend fitting to make noisy patterns easier to
interpret.

## Business Problem

Electricity costs can vary with appliance usage, operating hours, tariff rates,
location, and other operational factors. This project provides a reproducible
starting point for understanding those changes and identifying broad trends
that can support budgeting, monitoring, and further energy-efficiency analysis.

## Objectives

- Inspect electricity-consumption and billing data with Pandas.
- Smooth short-term variation using rolling mean averages.
- Estimate the overall direction of electricity bills and monthly hours with
  first-degree polynomial fitting (`numpy.polyfit`).
- Visualize raw observations, smoothed series, and fitted trend lines.
- Create a foundation for deeper analysis by city, company, month, appliance,
  or tariff rate.

## Tech Stack

- **Python**
- **Jupyter Notebook**
- **Pandas** for data loading and tabular analysis
- **NumPy** for numerical operations and linear trend fitting
- **Matplotlib** for visualizations

## Dataset

The notebook expects a CSV file named `electricity_bill_dataset.csv` with
columns such as:

`Fan`, `Refrigerator`, `AirConditioner`, `Television`, `Monitor`,
`MotorPump`, `Month`, `City`, `Company`, `MonthlyHours`, `TariffRate`, and
`ElectricityBill`.

The analyzed notebook contains 45,345 records. Keep the source dataset local
unless you have permission to redistribute it, and update the loading path in
the notebook for your local environment.

## Key Insights and Visualizations

The notebook produces two main trend visualizations:

1. **Electricity bill trend** - overlays the raw bill values, a 1,000-row
   moving average, and a fitted linear trend line.
2. **Monthly-hours trend** - overlays the raw monthly-hours values, a
   1,000-row moving average, and a fitted linear trend line.

The moving averages reduce short-term noise and make the underlying direction
easier to inspect. The fitted slope is printed for both measures and labeled
as an `UPTREND` or `DOWNTREND`. Because the trend is fitted against the
dataset row index rather than a calendar date, interpret it as an ordering
trend; use a date column for calendar-based time-series conclusions if one is
available.

Suggested portfolio screenshots to add:

- `images/electricity-bill-trend.png`
- `images/monthly-hours-trend.png`

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>
```

### 2. Create and activate a virtual environment (recommended)

Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install pandas numpy matplotlib jupyter
```

### 4. Add the dataset

Place `electricity_bill_dataset.csv` in the project directory, or change the
`pd.read_csv(...)` path in the notebook to the location of your data.

### 5. Launch Jupyter

```bash
jupyter notebook
```

Open `Electricity_consumption_dataset_trend_analysis (2).ipynb` and run the
cells from top to bottom.

## Repository Structure

```text
.
├── Electricity_consumption_dataset_trend_analysis (2).ipynb
├── electricity_bill_dataset.csv   # local/private data; do not commit by default
├── README.md
└── .gitignore
```

## Future Improvements

- Replace the row index with a true date column for calendar-aware analysis.
- Compare trends by city, company, appliance, and month.
- Add correlation and regression analysis for hours, tariff rates, and bills.
- Add data validation, missing-value checks, and automated chart export.

## License

Add a license that matches your intended use before publishing the project.
