## 🌍 Interactive CO₂ Emissions Dashboard ##

An interactive data visualization tool built with [Panel](https://panel.holoviz.org/) and [hvPlot](https://hvplot.holoviz.org/), designed to explore global and continental CO₂ emissions across time and source.

**CO₂ emissions per capita** 
Carbon dioxide (CO₂) emissions from burning fossil fuels and industrial processes. This includes emissions from transport, electricity generation, and heating, but not land-use change.  

_Data sources: Global Carbon Budget (2024)Population based on various sources (2024) – with major processing by Our World in Data_
Avialable at: https://ourworldindata.org/co2-and-greenhouse-gas-emissions#explore-data-on-co2-and-greenhouse-gas-emissions

## 📦 Project Structure 
 
 

Dashboard_A1/ ├── Interactive_CO2_Dashboard_A1.ipynb # Main dashboard notebook ├── Interactive_CO2_Dashboard_A1.py # Script version for deployment ├── requirements.txt # Reproducible environment ├── README.md # This guide ├── data/ # Optional: CSVs, GeoJSONs ├── assets/ # Optional: logos, icons └── venv/ # Virtual environment 

 
--- 
 
## ⚙️ Setup Instructions 
 
### 1. Clone or download the repository 
 
```bash 
git clone https://github.com/gerblogasgrace/co2_data_a1.git 
cd CO2-Dashboard 
 

2. Create and activate a virtual environment 

python -m venv venv 
.\venv\Scripts\Activate.ps1   # Windows PowerShell 
 

3. Install dependencies 

pip install -r requirements.txt 
 

If requirements.txt is missing, install manually: 

pip install panel pandas hvplot jupyterlab 
 

 

🚀 Run the Dashboard 

Option A: From Notebook (JupyterLab) 

jupyter lab 
 

Open Interactive_CO2_Dashboard_A1.ipynb and run all cells. 

Option B: As a Script (Panel App) 

panel serve Interactive_CO2_Dashboard_A1.py --show --autoreload 
 

Or use a custom port: 

panel serve Interactive_CO2_Dashboard_A1.py --port 5007 --show --autoreload 
 

 

🧠 Features 

📊 Dynamic CO₂ plots by year, continent, and source 

🧭 Semantic toggles for coal, oil, and gas emissions 

🌐 Modular pipelines for scalable data integration 

🧩 Widget-driven interactivity with Panel 


