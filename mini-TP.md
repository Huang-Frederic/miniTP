# Mini Project – Dash App & Data Cleaning 

**Estimated time**: 1 to 1.5 hours  

---

## Context

You are working for a fictitious subsurface data company. You’ve received a CSV file with borehole measurements from various locations. Unfortunately, the dataset is messy and needs cleaning before it can be used.

You are asked to:
- Clean the data using Python
- Build a small Dash web application to visualize the cleaned dataset
- Organize and version your code using Git
- Structure your code to make it modular (don't repeat yourself !).
- (Bonus) Deploy the app to a cloud platform

---

## What You’re Given

A CSV file: `boreholes_dirty.csv`  
This file contains around 150 borehole records with the following columns:
- `well_id`: ID of the borehole
- `depth_m`: depth (in meters)
- `lithology`: rock type
- `porosity`: rock porosity (0 to 1)
- `permeability`: rock permeability
- `operator`: company responsible
- `location`: field name
- `measurement_date`: date of measurement

⚠ The dataset includes:
- typos (e.g. `"Sandstne"`, `"SHALE"`)
- missing or invalid values (`"na"`, `"--"`, `None`)
- inconsistent types (e.g. depth as text)
- invalid or unknown dates

---

## What You Need to Do

You must complete **each step** below and make **a commit** when it's needed to keep a **clean environnement**.

---

### Step 1 – Project Setup

Create a new Python project with:
<!-- - A virtual environment -->
- A `requirements.txt` listing used libraries (e.g. `pandas`, `dash`, `plotly`)
- A `.gitignore` (to exclude `__pycache__`, `.venv/`, etc.)
- A `README.md` describing your app

---

### Step 2 – Data Cleaning

Create a file (`clean_data.py`) a script that:
- Loads `boreholes_dirty.csv` using `pandas`
- Fixes data types (e.g., numeric fields)
- Standardizes values (e.g., fix typos in `lithology`)
- Handles missing/invalid values
- Outputs a clean version of the dataset: `boreholes_clean.csv`

Tips :
- Use `str.strip()`, `str.lower()`, `.replace()` for cleaning text
- Use `dropna()` or fill values where appropriate

⚠ You should NOT in any way modify the original file `boreholes_dirty.csv` in the scope of this exercise.

---

### Step 3 – Create a Dash App

Build a Dash app that:
- Loads and uses `boreholes_clean.csv`
- Displays at least:
  - A histogram of `depth_m`
  - A scatter plot of `porosity` vs `permeability`
- Filtered Table : 
  - Depth range (`depth_m` > X)
  - Lithology (multi-select : X and Y only)
  - Operator (multi-select : Z only)
- Additional metrics if you think it's relevant.

⚠ Don't forget the structure of your app

---

### Step 4 – (Bonus) Cloud Deployment

Deploy your Dash app on a public platform like [Render](https://render.com/) (recommended), [Heroku](https://www.heroku.com/), or [Railway](https://railway.app/).

⚠ Document how to deploy the app in your `README.md`

---

## Step 5 - Final Report

Include a short report (`report.md` or `report.pdf`) answering:
- What steps you completed
- Any issues or bugs you encountered
- What you learned from this exercise
- Any feedback or suggestions

---

## Deliverables

You must submit:
- A link to your GitHub repository (leave it public so we have access)
- The cleaned dataset `boreholes_clean.csv`
- Your Dash app
- (Bonus) The steps to deploy on cloud (README.md)
- The Feedback Report

---

## Good luck!

Feel free to use external documentation (Dash, Plotly, Pandas ...) if needed. The goal is not to memorize everything, but to demonstrate your reasoning, code clarity, and ability to structure and deliver a small full-stack project.

🚀 Have fun!

