# Time Series & Analysis Projects

A portfolio collection of Python and Jupyter Notebook projects focused on
exploratory data analysis, time-series trends, forecasting foundations, and
clear visual storytelling.

The projects use real-world-style datasets to demonstrate practical work with
Pandas, NumPy, Matplotlib, Seaborn, and selected machine-learning utilities.

## Projects

| Project | Focus | Main techniques |
|---|---|---|
| [Electricity consumption trend analysis](./Electricity_consumption_dataset_trend_analysis%20%282%29.ipynb) | Electricity bills and operating hours | Rolling averages, `numpy.polyfit`, trend visualization |
| [Stock trend analysis](./Stock_trend_analysis%20%282%29.ipynb) | NIFTY 50 market data | Resampling, OHLC data, SMA, RSI, returns, volatility |
| [Tourism dataset prediction](./Tourism_dataset_prediction%20%282%29.ipynb) | Visitors and tourism revenue | Rolling averages, linear trends, visualization |
| [Weather dataset analysis](./Weather_Forecasting_Dataset%20%281%29.ipynb) | Weather conditions and measurements | Datetime conversion, descriptive statistics, filtering, plots |
| [Sales dataset analysis](./perform_numpy_%2C_pandas_and_matplotlib_on_sales_dataset%20%281%29.ipynb) | Product sales and profit | Pandas operations, NumPy statistics, Matplotlib charts |

## Skills Demonstrated

- Loading and inspecting CSV and Excel datasets
- Cleaning and converting date/time fields
- Resampling high-frequency data into daily summaries
- Computing moving averages and linear trend lines
- Measuring returns, volatility, and RSI-style indicators
- Filtering, grouping, and summarizing business data
- Building readable analytical visualizations
- Using numerical summaries to support data-driven conclusions

## Technology Stack

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **scikit-learn** for selected evaluation metrics

## Featured Analysis: Electricity Consumption

The electricity notebook analyzes a dataset with appliance usage, month,
location, company, monthly hours, tariff rate, and electricity bill fields.
It contains 45,345 records and applies a 1,000-row rolling average to
`ElectricityBill` and `MonthlyHours`.

The notebook also fits first-degree polynomial trends with `numpy.polyfit`
and produces charts comparing:

- Raw electricity bill values, a moving average, and a fitted trend
- Raw monthly-hours values, a moving average, and a fitted trend

The trend is fitted against the dataset row index rather than a calendar date,
so it should be interpreted as an ordering trend unless a date field is added.

## How to Run

### Clone the repository

```bash
git clone https://github.com/HARSH-7858/Time-series-Analysis-Projects.git
cd Time-series-Analysis-Projects
```

### Create a virtual environment

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

### Install dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

### Add the datasets

The notebooks currently reference datasets from their original execution
environment. Place the required files in the project directory and update the
loading paths in each notebook:

| Notebook | Expected input |
|---|---|
| Electricity | `electricity_bill_dataset.csv` |
| Stock | `nifty50.csv` |
| Tourism | `tourism_dataset.csv` |
| Weather | `Project1WeatherDataset.csv` |
| Sales | `sales_data_20 (1).xlsx` |

The source datasets are not included by default. Do not commit data that is
private, licensed, or otherwise restricted.

### Launch Jupyter

```bash
jupyter notebook
```

Open a notebook and run its cells from top to bottom. Google Colab users can
upload the required dataset when prompted or update the file paths for the
Colab session.

## Repository Structure

```text
.
├── Electricity_consumption_dataset_trend_analysis (2).ipynb
├── Stock_trend_analysis (2).ipynb
├── Tourism_dataset_prediction (2).ipynb
├── Weather_Forecasting_Dataset (1).ipynb
├── perform_numpy_,_pandas_and_matplotlib_on_sales_dataset (1).ipynb
├── README.md
└── .gitignore
```

## Future Improvements

- Add reusable Python modules instead of keeping all analysis inside notebooks.
- Add data dictionaries and source links for each dataset.
- Replace row-index trends with true date-based time-series models where dates
  are available.
- Add automated notebook execution and validation.
- Export selected charts for use in project summaries and dashboards.

## License

Add a license that matches the intended use and redistribution rights for this
portfolio repository.
