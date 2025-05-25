# Сравнение цен на продукты: Россия vs. Вьетнам

В этом проекте исследуются цены на продукты в **четырёх сетях супермаркетов** — *Пятерочка* и *Лента* в России, *WinMart* и *Co.op* во Вьетнаме — в 31 категории повседневных товаров.
Проект сравнивает цены в двух странах и представляет результаты в виде подробного анализа и интерактивных графиков.

Чтобы **посмотреть результаты**, [нажмите сюда](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) (Tableau Public).

> *Совет:*
> *1) нажмите кнопку «See this in full screen» в правом нижнем углу*
> *2) пролистывайте слайды и наводите мышь на элементы графиков, чтобы узнать больше*

Чтобы **вникнуть в детали**, обратитесь к подробным описаниям в ноутбуках (Jupyter Notebooks):
- Сбор данных: [Пятерочка](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/1_scraping_pyaterochka/scraping_pyaterochka.ipynb), [Лента](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/2_scraping_lenta/scraping_lenta.ipynb), [Winmart](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/3_scraping_winmart/scraping_winmart.ipynb), [Co.op](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/4_scraping_coop/scraping_coop.ipynb)
- [Объединение и очистка данных](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb)
- [Анализ](https://nbviewer.org/github/kolokol-sa/ru-vn-food-prices/blob/7e972869e595b388ad4c1e940f23043246e74964/5_6_cleaning_and_analysis/analysis.ipynb)
> *Совет: чтобы сделать код интерактивным, нажмите "Execute on Binder" в верхнем правом углу*

👇 **В описании ниже** можно узнать больше об идее проекта, выборе продуктов для анализа и структуре файлов.

## 🧠 Идея проекта

Как человек, переехавший из России во Вьетнам, я представляю себе разницу в ценах на продукты между ними. Но мне было интересно измерить эту разницу более точно и показать результаты в форме, которая будет понятной и наглядной для всех.

Также этот проект - часть моего портфолио аналитика данных, и он помог прокачать практические навыки:

- **Python** для скрейпинга и автоматизации
- **pandas** для очистки и обработки данных
- **Jupyter Notebook** для документирования процесса
- **Tableau**  для создания интерактивных визуализаций

## 🧃 Выбор категорий и типов продуктов

Чтобы оценить реальную картину цен на продукты, я выбрал 31 категорию основных продуктов, которые широко востребованы как в России, так и во Вьетнаме.

Многие из категорий - это универсальные продукты (например, молоко, яйца, рис), но некоторые специфичны для одной страны — например, гречка для России и водяной шпинат для Вьетнама. Такой выбор помогает сбалансировать схожести и различия.

Для объективного сравнения внутри каждой категории я отсеивал некоторые подвиды товара, например:

- **Курица** (chicken): учитывалось только **куриное филе** — стандартный и сопоставимый продукт, представленный в обеих странах.
- **Молоко** (milk): сравнивалось только **обычное молоко**, без добавок и сахара (часто встречается во Вьетнаме).
- **Зеленый чай** (green tea): включались **все варианты зелёного чая**, в том числе с любыми добавками. Отчасти такие критерии выбора были субъективны, но я ориентировался на то, что люди обычно покупают чаи с разными вкусами, но не воспринимают их как разные продукты для разных ситуаций.

Эти фильтры позволили сделать данные более сопоставимыми, не усложняя анализ.

## 🗂️ Структура файлов

Проект организован по этапам проекта — от сбора данных до их очистки, анализа и визуализации. Ниже представлено, что входит в каждый раздел:

| **Этап проекта**           | **Файлы и папки** | **Описание** |
|-----------------------------|----------------------|----------------|
| 🛒 Сбор данных | [`1_scraping_pyaterochka`](1_scraping_pyaterochka/)<br>[`2_scraping_lenta`](2_scraping_lenta/)<br>[`3_scraping_winmart`](3_scraping_winmart/)<br>[`4_scraping_coop`](4_scraping_coop/)<br> | |
| | В каждой папке находятся:<br>• `categories-*.csv`<br>• `scraped_products-*.csv`<br>• `filtered_products-*.csv`<br>• `scraping_*.ipynb` | <br>– категорий продуктов с сайта супермаркета<br>– данные всех загруженных продуктов<br>– отобранные данные релевантных продуктов<br>– ноутбук с кодом и описанием сбора данных и фильтрации |
| 🧼 Объединение и очистка данных | [`5_6_cleaning_and_analysis`](5_6_cleaning_and_analysis/) | |
| | 4 x `filtered_products-*.csv`<br><br>[`aggregation_and_cleaning.ipynb`](5_6_cleaning_and_analysis/aggregation_and_cleaning.ipynb)<br><br>[`clean_products-2025-03-12-local.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-local.csv)<br>[`clean_products-2025-03-12-usd.csv`](5_6_cleaning_and_analysis/clean_products-2025-03-12-usd.csv) | – копии отфильтрованных данных из папок 1–4<br>– ноутбук с кодом и описанием очистки данных и подготовки к анализу<br><br>– финальный очищенный список продуктов (рубли и донги)<br><br>– то же, но цены в долларах |
| 📊 Анализ | [`5_6_cleaning_and_analysis`](5_6_cleaning_and_analysis/) | |
| | [`analysis.ipynb`](5_6_cleaning_and_analysis/analysis.ipynb)<br>[`data_general_summary`](5_6_cleaning_and_analysis/data_general_summary/)<br><br>[`data_by_category`](5_6_cleaning_and_analysis/data_by_category/)<br><br>[`category-comparison.csv`](5_6_cleaning_and_analysis/category-comparison.csv)<br><br>[`category_reports_v0`](5_6_cleaning_and_analysis/category_reports_v0/)<br>[`category_reports_v1`](5_6_cleaning_and_analysis/category_reports_v1/) | – ноутбук с кодом и описанием анализа <br>– сводные таблицы количества продуктов по странам, супермаркетам и категориям + подный список анализируемых продуктов<br>– списки продуктов и описательная статистика по категориям<br>– сводная таблица медианных цен и соотношений цен (VN/RU) по категориям<br>– детальные выводы по категориям<br>– краткие ключевые наблюдения по категориям | 
| 📈 Визуализация | Доступна в [Tableau Public](https://public.tableau.com/views/GroceryPricesRussiavs_Vietnam/Final?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) |
