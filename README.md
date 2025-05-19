# youtube-analytics
📊 YouTube Trending Video Analytics – README
🧠 Project Overview
This project analyzes trending YouTube videos across multiple countries to uncover patterns in content popularity, sentiment, and regional trends using Python, SQL, and visualization tools.

🔧 Tools & Libraries
Python: Data cleaning, sentiment analysis, visualization

SQLite: Category-based ranking queries

Seaborn/Matplotlib: Visual insights

Pandas: Data handling

TextBlob: Sentiment analysis

Tableau: (External) for dashboarding

🌍 Datasets Used
CSV files from multiple regions:

USvideos.csv, INvideos.csv, GBvideos.csv, CAvideos.csv, MXvideos.csv, JPvideos.csv, DEvideos.csv

JSON file:

US_category_id.json (used for mapping category names)

📁 Project Pipeline
1. Data Import & Cleaning
Loaded regional CSVs into a combined DataFrame

Removed duplicates and nulls

Standardized column names

Unified category_id using JSON mapping

2. Sentiment Analysis
Analyzed video titles using TextBlob

Classified sentiment into: positive, neutral, negative

3. Trending Duration Calculation
Calculated number of days between publish and trending dates

4. SQL Integration
Saved cleaned data to SQLite database

Queried average views by category

5. Visualizations
Generated multiple plots:

📉 Views vs Likes (scatter, log scale)

📦 Boxplot of Views by Category

😊 Sentiment Distribution Count Plot

⏱️ Trending Duration Histogram

Note: Some visualizations throw a FutureWarning due to upcoming seaborn changes — no impact on output now.

6. Export
Cleaned dataset saved as cleaned_youtube_trending.csv for Tableau or further use.

📌 Output Files
cleaned_youtube_trending.csv – Final cleaned dataset

youtube_trending.db – SQLite DB with full video table

Visual charts (optional: screenshots or Tableau dashboard exports)

✅ How to Run
Ensure all CSV and JSON files are in the same directory.

Run the Python script.

Use the exported CSV in Tableau or any BI tool for dashboarding.

📈 Sample Insights
Top Category: Music had the highest average views globally.

Sentiment: Most titles were positive or neutral.

Regional Trends: US and CA led in video volume; JP trailed with the fewest.

Trending Duration: Most videos trend 1–7 days post-publishing.

