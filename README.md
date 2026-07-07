# UK Cross-Asset Market Monitor
This project creates a weekly cross-asset summary table using Python and Yahoo Finance data. The notebook tracks major equity indicies, FX pairs, commodities, volatility, and bond yields. It calculates weekly market moves from Monday open to Friday close.

## Assets covered
The monitor currently tracks:

- FTSE 100
- FTSE 250
- S&P 500
- VIX
- Brent Crude
- GBP/USD
- EUR/GBP
- US 10Y Treasury Yield

## What the notebook does

The notebook produces a weekly summary table tracking:

- Monday Open
- Friday Close
- Weekly Change
- Weekly % Change
- Change in basis points for the US 10Y Treasury Yield

Bond yields are treated differently to the regular price assets. For the US 10Y Treasury Yield, the weekly move is shown in basis points instead of percentage change.

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

First, run all cells in notebook.

Then generate a weekly table by running:
create_weekly_summary_for_week("date")

Use dates in this format:
"YYYY-MM-DD"

For example:
create_weekly_summary_for_week("2026-07-01")

This will create a table for the most recent completed trading week ending on or before that date.

To generate the latest available week run:
create_weekly_summary_for_week()