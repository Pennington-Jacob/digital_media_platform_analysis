**Steam Market Analysis: Game Publisher Strategy Dashboard**
A Power BI project evaluating Steam market trends to help video game publishers analyze pricing, player engagement, and sentiment across genres and categories.

**Overview**
This project transforms raw Steam data to answer three publisher questions:
Price vs. Playtime: What price points yield the highest player engagement?
Review Sentiment: How do review scores vary across pricing tiers?
Localization & Reach: How do language support, OS compatibility, and categories impact game volume?

**Tools Used**
Data Sources: Primary Steam dataset (Kaggle) merged with historical review stats via appid.
ETL & Data Transformation: Excel and Power Query
Visualization: Power BI

**Data Cleaning & Transformation**
Filtered Inactive Listings: Removed 30,000+ zero-review/zero-playtime entries to isolate active games.
Dropped Irrelevant Metadata: Stripped out support links, Metacritic URLs, and website fields.
Fixed Schema Mismatches: Corrected shifted columns using official Steam API documentation.
Dataset Join: Merged historical review metrics on appid.
String Cleaning: Removed list syntax ({, }, ', [, ]) from array fields.
Unpivoted Attributes: Unpivoted multi-value columns (Genres, Categories, Supported Languages) to normalized vertical rows locked to appid.
Type Casting: Mapped dates, numeric IDs, prices/DLCs (decimals), and platform support flags (booleans).

**Key Metrics & Insights**
Catalog Baseline: ~95,000 games analyzed | $10.70 average price | 243.61 average lifetime hours.
Category Price Drivers: Titles with Steam Trading Cards carry the highest average price point.
Genre Volume: Action dominates overall catalog size (~35k+ games), followed by Indie, Adventure, and Casual.
Playtime Variance Under $20: Sub-$20 titles show the highest engagement peaks (8k–15k+ avg hours) and widest playtime variance, whereas 40–80 titles show flatter engagement.
Sentiment Concentration: High positive review counts (up to 500k+) cluster heavily in the 0–30 price band.

**Dashboard Visualizations & Filters**
KPI Summary Cards: Total catalog games (95K), average price ($10.70), and average playtime metrics.
Bar & Line Charts: App count by genre, playtime vs. price curves, and historical annual releases (2010–2025).
Scatter Plot: Price vs. positive review volume up to $150.
Category Treemap: Average price comparison across feature tags (Trading Cards, VR, Remote Play).
Interactive Slicers: Dynamic filters for categories, OS support (linux, mac, windows), and supported languages.
