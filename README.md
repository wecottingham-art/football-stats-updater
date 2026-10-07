# football-stats-updater
Pitch Metrics
A live analytics platform for comparing top-5 European league football players using dynamic visualizations (Scatter Plots, Bar Charts, and Radar Charts) powered by scrapers fetching data from FotMob and ESPN.

Features
Live Scraper Engine: Collects live match and season statistics for Europe's top 5 leagues.
Interactive Multi-Player Comparison: Choose up to 50 players simultaneously on scatter plots or individual head-to-head comparisons.
Per 90 Normalization Toggle: Switch effortlessly between raw totals and Per 90 metrics ((Stat / Minutes Played) * 90).
3 Dynamic Visualization Modes:
Scatter Plot: Compare 2 custom metrics (e.g., Attempted Passes vs. Completed Passes or xG vs. Actual Goals).
Bar Graph: Rank selected players side-by-side on any selected stat.
Radar Chart: Multi-axis positional profile comparison.
Tech Stack
Data Scraping & ETL: Python, requests, pandas, BeautifulSoup4
Backend: FastAPI, SQLAlchemy, SQLite/PostgreSQL
Frontend: React (Vite/Tailwind CSS), Recharts, Lucide Icons
Quickstart Guide
1. Backend & Scraper Setup
# Clone repository
git clone https://github.com/your-username/pitch-metrics.git
cd pitch-metrics

# Create virtual environment
python -m venv venv
source venv/bin/activate # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run Scraper to populate local database
python scraper/fotmob_scraper.py

# Launch FastAPI Server
uvicorn backend.main:app --reload
