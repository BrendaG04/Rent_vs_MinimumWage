# US Housing Affordability Analysis: Minimum Wage vs. Fair Market Rent

A comprehensive data analysis project examining the relationship between minimum wage and housing affordability across the United States using 2024 Fair Market Rent data.


## Project Overview

This team project investigates a critical question: **Can minimum wage workers afford rent in America?**

Using 2024 Fair Market Rent data from HUD and state-level minimum wage information, we analyze housing affordability across all 50 U.S. states, revealing significant gaps between what workers earn and what housing costs.

### Key Finding
> **Not a single U.S. state allows a minimum-wage worker to independently afford a 1-bedroom apartment** based on the standard 30% income-to-rent ratio.

## Research Questions

- How many hours of minimum wage work are required to afford average rent?
- Which states have the worst/best housing affordability?
- What is the relationship between rent prices and affordability?
- How does affordability vary by home size (studio, 1-bed, 2-bed, etc.)?
- What is the income gap for minimum wage workers?

## Dataset Sources

### Fair Market Rent (2024)
**U.S. Department of Housing and Urban Development (HUD)**
- **API:** [HUD User FMR API](https://www.huduser.gov/portal/dataset/fmr-api.html)
- Contains rent data for metro areas and counties across all 50 states
- Includes studio, 1-bed, 2-bed, 3-bed, and 4-bed rental prices

### Minimum Wage by State
**Rich States, Poor States**
- **Source:** [State Minimum Wage Data](https://www.richstatespoorstates.org/variables/state_minimum_wage/)
- Web scraped hourly wage data for all 50 states

## Technologies Used

**Python**

**Libraries:**
- `pandas` - Data manipulation and analysis
- `BeautifulSoup` - Web scraping for minimum wage data
- `requests` - API calls and HTTP requests
- `matplotlib` - Static data visualizations
- `seaborn` - Statistical data visualization
- `plotly` - Interactive visualizations
- `scipy` - Statistical analysis and outlier detection

## Getting Started

### Prerequisites

Install required packages:
```bash
pip install pandas beautifulsoup4 requests matplotlib seaborn plotly scipy
```

### Setting Up API Access

This project requires a **HUD User API key**.

**Steps:**

1. Register for a free API key at [HUD User API Registration](https://www.huduser.gov/portal/dataset/api-terms.html)

2. In **Google Colab**, add your API key to Secrets:
   - Click the **🔑 key icon** in the left sidebar (Secrets)
   - Click **"Add new secret"**
   - **Name:** `HUD_API_KEY`
   - **Value:** Your actual API key
   - Toggle on **"Notebook access"**

3. The notebook accesses it securely using:
```python
from google.colab import userdata
api_key = userdata.get('HUD_API_KEY')
header = {"Authorization": f"Bearer {api_key}"}
```

### Running the Notebook

1. Open the notebook in Google Colab
2. Add your HUD API key to Colab Secrets
3. Run all cells in order
4. The notebook will:
   - Fetch data from HUD API
   - Scrape minimum wage data
   - Merge datasets
   - Perform data cleaning
   - Calculate affordability metrics
   - Generate visualizations
   - Export CSV files

## Final Summary

**The data tells a very clear story:**

- Minimum wage is far below what is needed to afford rent in every state
- Rent varies dramatically, wages barely vary at all
- Even the "best" states are still unaffordable
- Outlier states push the averages even higher
- The upward trend of rent vs hours needed is unmistakable: high rent = impossible affordability

This project reveals how severe the housing crisis truly is for low-income workers. Using real government datasets and strong visualizations, our conclusions are backed by actual evidence.


