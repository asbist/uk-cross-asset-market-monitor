# UK Cross-Asset Market Monitor

This project creates a weekly cross-asset market summary using Python and Yahoo Finance data. The notebook tracks major equity indices, FX pairs, commodities, volatility, and bond yields, calculating weekly market moves from Monday open to Friday close.

The project is designed to support a six-week UK market report by creating a repeatable process for monitoring cross-asset price action, identifying market themes, and exporting weekly snapshots to Excel for ongoing analysis.

## Assets Covered

The monitor currently tracks:

- FTSE 100
- FTSE 250
- S&P 500
- VIX
- Brent Crude
- GBP/USD
- EUR/GBP
- US 10Y Treasury Yield

## What the Notebook Does

The notebook produces a weekly summary table showing:

- Monday Open
- Friday Close
- Weekly Change
- Weekly % Change
- Change in basis points for the US 10Y Treasury Yield

Bond yields are treated differently from regular price assets. For the US 10Y Treasury Yield, the weekly move is shown in basis points rather than as a percentage change.

The notebook also exports weekly snapshots to an Excel workbook, allowing a historical record of weekly market moves to build over time.

## Features

- Downloads market data using `yfinance`
- Tracks weekly moves from Monday open to Friday close
- Covers equities, FX, commodities, volatility, and bond yields
- Calculates percentage moves for price-based assets
- Calculates basis point moves for bond yields
- Exports weekly market snapshots to Excel
- Avoids duplicate weekly entries when the same week is exported more than once

## Installation

You can run this notebook using any Python notebook environment, such as:

- Jupyter Notebook
- JupyterLab
- Google Colab
- Visual Studio Code
- Anaconda Navigator

### Step 1: Download the project

Download or clone this GitHub repository onto your computer.

On GitHub, you can click:

Code > Download ZIP

Then unzip the folder.

### Step 2: Install the required packages

Open a terminal or command prompt in the project folder and run:

```bash
pip install -r requirements.txt
```


## How to use the notebook

First, run all cells in the notebook.

Then generate a weekly table by running:

```python
weekly_summary, week_start, latest_friday = create_weekly_summary_for_week("2026-07-03")

weekly_summary
```

Use dates in this format:

```text
YYYY-MM-DD
```

To export a weekly table to Excel, run:

```python
export_week_to_excel("2026-07-03")
```

To export the latest completed week, run:

```python
export_week_to_excel()
```