# CPO Crude Palm Oil Forecast Dashboard

This is a basic dashboard built with Streamlit to forecast CPO prices and estimate export tax and levy based on those forecasts. The app uses a SARIMAX model to generate price projections and applies a simple rule-based system to estimate taxes.

## What it does

- Forecasts CPO prices up to 12 months ahead
- Calculates export tax and levy based on forecasted prices
- Displays charts of historical and future prices
- Offers weekly export tax summaries
- Allows download of forecasted data as Excel file

## How tax is calculated

| Price (USD/ton) | Export Tax (%) | Levy (USD) |
|------------------|----------------|-------------|
| ≤ 680            | 0              | 0           |
| 681–730          | 3              | 15          |
| 731–780          | 8              | 52          |
| > 780            | 18             | 85          |

## Tech stack

- Python
- Streamlit
- pandas, numpy, statsmodels
- matplotlib, altair
- xlsxwriter (for Excel download)

## How to run

1. Clone the repo

```
git clone https://github.com/dsimanj2/CPO_Crude_Palm_Oil_Forecast_Dashboard.git
cd CPO_Crude_Palm_Oil_Forecast_Dashboard
```

2. Install dependencies

```
pip install -r requirements.txt
```

3. Launch the app

```
streamlit run app.py
```

## Requirements

```
streamlit
pandas
numpy
matplotlib
altair
statsmodels
xlsxwriter
```

## Notes

- This uses dummy/simulated data for now
- Model can be swapped with actual CPO price data and tax rules if available
- Focus is on basic functionality, not live production

## Author

Denny Simanjuntak  
github.com/dsimanj2
