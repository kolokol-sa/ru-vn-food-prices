# Grocery Price Comparison: Russia vs. Vietnam

This project explores grocery prices in **four supermarket chains** — *Pyaterochka* and *Lenta* in Russia, *WinMart* and *Co.op* in Vietnam — across 31 everyday product categories.
It compares costs between the two countries and presents the results through structured analysis and interactive visualizations.  

▶️ To explore the results, view the [interactive Tableau Story](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).  
> *Tip: click through slides and hover over elements to see more detail.*  

🧩 To follow the process, see the core notebooks:
- Scraping: [Pyaterochka](1_scraping_pyaterochka/scraping_pyaterochka.ipynb), [Lenta](2_scraping_lenta/scraping_lenta.ipynb), [Winmart](3_scraping_winmart/scraping_winmart.ipynb), [Co.op](4_scraping_coop/scraping_coop.ipynb)
- [Aggregation & Cleaning](5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb)
- [Analysis](5_6_cleaning_and_analysis/analysis.ipynb)

👇 **See the sections below** for more background on the project’s motivation, product selection approach, and detailed repository structure.

## Project Motivation

As someone who moved from Russia to Vietnam, I'm personally familiar with the difference in grocery prices between the two countries. While I had a general sense of the price gap, I was curious to quantify it and present the results in a clear, visual, and shareable format.

The project also served as a portfolio piece to sharpen my practical skills in:

- **Python** for web scraping and automation
- **pandas** for data cleaning and transformation
- **Jupyter Notebook** for documenting the workflow
- **Tableau** Public for building interactive visualizations
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

| **Workflow Step**           | **Files & Folders**                                                                 |
|----------------------------|--------------------------------------------------------------------------------------|
| 🛒 Data Scraping<br><br><br><br><br><br><br><br><br><br> | [`1_scraping_pyaterochka`](1_scraping_pyaterochka/)<br>[`2_scraping_lenta`](2_scraping_lenta/)<br>[`3_scraping_winmart`](3_scraping_winmart/)<br>[`4_scraping_coop`](4_scraping_coop/)<br>Each folder includes:<br>• `categories-*.csv` – product categories from the supermarket site<br>• `scraped_products-*.csv` – full scraped product data<br>• `filtered_products-*.csv` – filtered relevant items<br>• `scraping_*.ipynb` – Jupyter notebook documenting scraping and filtering<br>_Note: `4_scraping_coop` also contains a sample HTML file used to extract categories._ |
| 🧼 Aggregation & Cleaning<br><br><br><br> | [`5_6_cleaning_and_analysis`](5_6_cleaning_and_analysis/)<br>4x `filtered_products-*.csv` – consolidated filtered product lists from folders 1–4<br>[`aggregation_and_cleaning.ipynb`](5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb) – notebook documenting cleaning and preparation for analysis<br>[`clean_products-2025-03-12-local.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-local.csv) – final cleaned product list (local currencies)<br>[`clean_products-2025-03-12-usd.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-usd.csv) – same, converted to USD |
| 📊 Exploratory Analysis<br><br><br><br><br><br><br> | [`analysis.ipynb`](5_6_cleaning_and_analysis/analysis.ipynb) – exploratory data analysis notebook<br>[`data_general_summary`](5_6_cleaning_and_analysis/data_general_summary/) – aggregated stats by country, supermarket, and category<br>[`data_by_category`](5_6_cleaning_and_analysis/data_by_category/) – item lists & summary stats per category<br>[`category-comparison.csv`](5_6_cleaning_and_analysis/category-comparison.csv) – summary table of median prices by category & country, plus VN/RU price ratios<br>[`category_reports_v0`](5_6_cleaning_and_analysis/category_reports_v0/) – full write-ups per category<br>[`category_reports_v1`](5_6_cleaning_and_analysis/category_reports_v1/) – condensed key points used in Tableau Story |
| 📈 Visualization | Available in [Tableau Public](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) |

## About the Author
I’m a self-driven data enthusiast working on portfolio projects to deepen my understanding of real-world data analysis. This project reflects my curiosity, analytical mindset, and attention to detail.
