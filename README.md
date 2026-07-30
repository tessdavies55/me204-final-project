# ME204 Final Project: [European Air Quality and Weather]

| GitHub username | LSE ID |
|-----------------|--------|
| `tessdavies55` | `2026250086300` |

## Overview

This project investigates the question:

**How does air quality vary across major European cities, and which weather conditions are associated with worse pollution?**

The project compares air-quality and weather measurements across ten European cities:

- London
- Paris
- Berlin
- Madrid
- Rome
- Amsterdam
- Brussels
- Vienna
- Copenhagen
- Prague

The analysis focuses on Air Quality Index categories, PM2.5, PM10, nitrogen dioxide, ozone, carbon monoxide, temperature, humidity, atmospheric pressure, and wind speed.

The results represent a snapshot of conditions at the time the data was collected. They show differences between cities and associations between variables, but they do not prove that weather caused the observed pollution levels.

## Data sources

The data was collected using the OpenWeather API.

Two API endpoints were used:

1. **Current Weather API**
   - Temperature
   - Humidity
   - Atmospheric pressure
   - Wind speed

2. **Air Pollution API**
   - Air Quality Index
   - PM2.5
   - PM10
   - Nitrogen dioxide
   - Ozone
   - Carbon monoxide

Each city was identified using its latitude and longitude.

## How to reproduce

To reproduce this project, you will need Python 3, the required Python packages, and an OpenWeather API key.

### 1. Clone the repository

Clone the GitHub repository and navigate to the project folder:

```bash
git clone <repository-url>
cd final-project
```

### 2. Install the required packages

Install the Python packages used throughout the project:

```bash
python3 -m pip install requests pandas python-dotenv matplotlib
```

### 3. Obtain an OpenWeather API key

Create a free account at https://openweathermap.org/ and generate an API key.

In the root of the project, create a file named `.env` containing:

```text
OPENWEATHER_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your own API key. The `.env` file is excluded from Git using `.gitignore`, so your key will remain private.

### 4. Run the notebooks

Run the notebooks in the following order:

1. `NB01-Data-Collection.ipynb`
2. `NB02-Data-Transformation.ipynb`
3. `NB03-Data-Analysis.ipynb`

NB01 connects to the OpenWeather API and saves the raw JSON responses in `data/raw`.

NB02 loads the raw data, extracts the relevant variables, cleans the dataset, and saves the processed CSV in `data/processed`.

NB03 reads the processed dataset, creates summary statistics and visualizations, and saves the figures to `docs/figures` for use on the GitHub Pages website.

### 5. View the website

After running all notebooks and pushing the repository to GitHub, enable GitHub Pages using the `docs` folder as the publishing source. The project website will display the final visualizations and key findings.

# me204-final-project
