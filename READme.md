
## Setup

### 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/sv_project.git
cd sv_project

### 2. Create a virtual environment
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Download external data files
The following files need to be downloaded manually and placed in data/raw/:

- EPU_index.csv — Daily Economic Policy Uncertainty index
  Download from: https://www.policyuncertainty.com/us_daily.html

- GPR_index.xls — Geopolitical Risk index
  Download from: https://www.matteoiacoviello.com/gpr.htm

## How to Run

Run the notebooks in order:

1. 01_raw_data_acquisition.ipynb — pulls SPX, FRED, and yfinance data
2. 02_candidate_variables.ipynb — constructs and standardizes all candidate variables

Output files will be saved to data/processed/:
- all_variables_raw.csv — all variables unstandarized
- all_variables_standardized.csv — all variables standardized (rolling expanding window)
- metadata.csv — variable descriptions, sources, and transformations

