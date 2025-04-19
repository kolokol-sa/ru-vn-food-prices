### Grocery Price Comparison: Russia vs. Vietnam

Goal:  
This project compares grocery prices across Russian and Vietnamese supermarkets, focusing on 31 everyday product categories. It aims to explore price differences, visualize cost disparities, and practice data collection, cleaning, and analysis — making it a comprehensive portfolio project for data analytics.

👉  View the Project Summary and Visualizations in Tableau [here](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) (Tableau Public)

### Project Motivation

As someone who moved from Russia to Vietnam, I'm personally familiar with the difference in grocery prices between the two countries. While I had a general sense of the price gap, I was curious to quantify it and present the results in a clear, visual, and shareable format.

The project also served as a portfolio piece to sharpen my practical skills in:

- **Python** for web scraping and automation
- **pandas** for data cleaning and transformation
- **Jupyter Notebook** for documenting the workflow
- **Tableau** Public for building interactive visualizations
- Data storytelling and communication

### Product Selection Criteria

To reflect a realistic picture of grocery prices, I selected 31 categories of essential food items that are widely available and consumed in both Russia and Vietnam.

While some categories represent universal staples (e.g., milk, eggs, rice), others highlight region-specific preferences, such as buckwheat for Russia and water spinach for Vietnam. These choices help capture both overlap and cultural variety in grocery shopping habits.

### Filtering Rules per Category

To ensure fair comparisons, I applied simple filtering rules within each category, based on product availability and typical consumer expectations:

- **Chicken:** Only chicken fillet was included — a standard cut available in both countries that reasonably represents overall chicken pricing.
- **Milk:** Only plain milk was used, excluding flavored or sweetened versions (commonly found in Vietnam) to focus on the base product.
- **Green Tea:** Included all loose-leaf green tea products, including flavored variations. While the definition is somewhat subjective, I considered all loose tea blends containing green tea as part of the same category, since they serve the same purpose for most consumers.

These filtering decisions helped improve consistency without overcomplicating the analysis.

### Repository Structure

The project is organized into folders corresponding to each stage of the workflow — from data collection to analysis and final insights:

📁 1_scraping_pyaterochka/
📁 2_scraping_lenta/
📁 3_scraping_winmart/
📁 4_scraping_coop/

Each of these folders contains:
- `categories-*.csv` — list of categories found on the supermarket site  
- `scraped_products-*.csv` — raw scraped product data  
- `filtered_products-*.csv` — filtered list with relevant items only  
- `scraping_*.ipynb` — scraping code used for that supermarket  
> *Note: `4_scraping_coop/` also includes a sample HTML file used to extract category data.*

📁 5_6_cleaning_and_analysis/

Contains cleaned data, analysis notebooks, and summary outputs:
- `aggregation_and_cleaning.ipynb` — cleaning and preprocessing steps  
- `analysis.ipynb` — exploratory analysis  
- `category-comparison.csv` — **final price comparison results** with median prices by country, category, and calculated VN/RU price ratios  
- `category_reports_v0/` — full written insights by category  
- `category_reports_v1/` — key points used in visualization  
- `data_by_category/` — per-category CSVs, including item lists and summary stats  
- `data_general_summary/` — overall stats (e.g., item counts by country, category, supermarket)  
- `clean_products-2025-03-12-local.csv` — final cleaned product list with prices in local currencies  
- `clean_products-2025-03-12-usd.csv` — same as above, with all prices converted to USD  
- `filtered_products-2025-03-03-pyaterochka.csv`  
  `filtered_products-2025-03-04-lenta.csv`  
  `filtered_products-2025-03-06-winmart.csv`  
  `filtered_products-2025-03-07-coop.csv`  
  — consolidated filtered product lists from folders 1–4  

### Visualization

The final results are presented as a **Tableau Story**, showcasing key insights and price differences between Russia and Vietnam.  
It highlights the most and least expensive categories, relative affordability, and other notable patterns observed in the data.

👉 [**View the Tableau Story**](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### About the Author
I’m a self-driven data enthusiast working on portfolio projects to deepen my understanding of real-world data analysis. This project reflects my curiosity, analytical mindset, and attention to detail.