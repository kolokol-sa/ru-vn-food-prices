# Grocery Price Comparison: Russia vs. Vietnam

[Версия проекта на русском языке](README_RU.md)

This project explores grocery prices in **four supermarket chains** — *Pyaterochka* and *Lenta* in Russia, *WinMart* and *Co.op* in Vietnam — across 31 everyday product categories.
It compares costs between the two countries and presents the results through structured analysis and interactive visualizations.  

To **explore the results**, view the [interactive Tableau Story](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).  
> *Tips:*  
> *1) click "See this in full screen" button at the bottom right corner*  
> *2) click through slides and hover over elements to see more detail*  

To **follow the process**, see the core notebooks:
- Scraping: [Pyaterochka](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/1_scraping_pyaterochka/scraping_pyaterochka.ipynb), [Lenta](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/2_scraping_lenta/scraping_lenta.ipynb), [Winmart](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/3_scraping_winmart/scraping_winmart.ipynb), [Co.op](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/4_scraping_coop/scraping_coop.ipynb)
- [Aggregation & Cleaning](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb)
- [Analysis](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/747c98f95b3e295d7ce7bbca019dffdf031fdd56/5_6_cleaning_and_analysis/analysis.ipynb)
> *Tip: to make the code interactive, click "Execute on Binder" button at the top right corner of the notebook.*

👇 **See the sections below** for more background on the project’s motivation, product selection approach, and detailed repository structure.

## 🧠 Project Motivation

As someone who moved from Russia to Vietnam, I'm personally familiar with the difference in grocery prices between the two countries. While I had a general sense of the price gap, I was curious to quantify it and present the results in a clear, visual, and shareable format.

The project also served as a portfolio piece to sharpen my practical skills in:

- **Python** for web scraping and automation
- **pandas** for data cleaning and transformation
- **Jupyter Notebook** for documenting the workflow
- **Tableau** for building interactive visualizations
- Data storytelling and communication

## 🧃 Product Selection & Filtering

To reflect a realistic picture of grocery prices, I selected **31 categories** of essential food items that are widely available and consumed in both Russia and Vietnam.

While many categories cover universal staples (e.g., milk, eggs, rice), a few represent region-specific preferences — for example, buckwheat buckwheat for Russia and water spinach for Vietnam. These choices aim to balance overlap with cultural variety.

To ensure fair comparisons, I applied basic filtering rules within each category, based on typical product availability and consumer expectations:

- **Chicken**: Only **chicken fillet** was included — a standard cut available in both countries that reasonably represents overall chicken pricing.
- **Milk**: Only **plain milk** was used, excluding flavored or sweetened versions (common in Vietnam), to focus on the base product.
- **Green Tea**: Included **all loose-leaf green tea products**, even flavored blends. While the inclusion criteria were somewhat subjective, I considered all such items as fulfilling a similar role in everyday tea consumption.

These filtering decisions improved consistency without overcomplicating the analysis.

## 🗂️ Repository Structure

The project is organized by workflow stage — from scraping data to cleaning, analysis, and insights. Here's a breakdown of what each part contains:

| **Workflow Step**           | **Files & Folders** | **Description** |
|-----------------------------|----------------------|----------------|
| 🛒 Data Scraping | [`1_scraping_pyaterochka`](1_scraping_pyaterochka/)<br>[`2_scraping_lenta`](2_scraping_lenta/)<br>[`3_scraping_winmart`](3_scraping_winmart/)<br>[`4_scraping_coop`](4_scraping_coop/)<br> | |
| | Each folder includes:<br>• `categories-*.csv`<br>• `scraped_products-*.csv`<br>• `filtered_products-*.csv`<br>• `scraping_*.ipynb` | <br>– product categories from the supermarket site<br>– full scraped product data<br>– filtered relevant items<br>– notebook documenting scraping and filtering |
| 🧼 Aggregation & Cleaning | [`5_6_cleaning_and_analysis`](5_6_cleaning_and_analysis/) | |
| | 4 x `filtered_products-*.csv`<br><br>[`aggregation_and_cleaning.ipynb`](5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb)<br><br>[`clean_products-2025-03-12-local.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-local.csv)<br>[`clean_products-2025-03-12-usd.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-usd.csv) | – consolidated filtered product lists from folders 1–4<br>– notebook documenting cleaning and preparation for analysis<br><br>– final cleaned product list (local currencies)<br><br>– same, converted to USD |
| 📊 Exploratory Analysis | [`5_6_cleaning_and_analysis`](5_6_cleaning_and_analysis/) | |
| | [`analysis.ipynb`](5_6_cleaning_and_analysis/analysis.ipynb)<br>[`data_general_summary`](5_6_cleaning_and_analysis/data_general_summary/)<br><br>[`data_by_category`](5_6_cleaning_and_analysis/data_by_category/)<br><br>[`category-comparison.csv`](5_6_cleaning_and_analysis/category-comparison.csv)<br><br>[`category_reports_v0`](5_6_cleaning_and_analysis/category_reports_v0/)<br>[`category_reports_v1`](5_6_cleaning_and_analysis/category_reports_v1/) | – exploratory data analysis notebook<br>– item counts by country, supermarket, category + full list of analyzed products<br>– item lists & summary stats (median, min, max, etc.) per category<br>– summary table of median prices and VN/RU price ratios by category & country<br>– detailed insights and observations per category<br>– condensed key points used in the visualization | 
| 📈 Visualization | Available in [Tableau Public](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) |
