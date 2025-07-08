China Diplomatic Visits Dashboard

This project analyzes the international diplomatic visits made by top Chinese leaders, focusing on Xi Jinping and other key figures like Premier Li Keqiang and Premier Li Qiang. The goal is to build a clean dataset from public sources and create an interactive visualization that reflects the frequency, purpose, and intensity of China's global engagements.

 Objective

To create a cleaned, classified, and visually informative dataset of China's diplomatic visits, categorized by intent and enriched with country classification. The final deliverables include both the processed dataset and Tableau dashboards for analysis.


Data Sources

Wikipedia: [Xi Jinping's International Trips](https://en.wikipedia.org/wiki/List_of_international_trips_made_by_Xi_Jinping)
CEIAS Diplomatic Tracker: [CEIAS Tracker](https://who-where-when.ceias.eu)
China’s MFA (Ministry of Foreign Affairs)**


Data Processing

- Scraped visit data using **Selenium** and **BeautifulSoup**
- Cleaned and standardized:

  * Country names
  * Leader titles
  * Date formats
- Grouped countries into: **Developed**, **Developing**, and **Communist**
- Removed duplicates and missing information



NLP-Based Visit Classification

Used the Facebook BART model (via Hugging Face Transformers) for **zero-shot text classification**. Each visit was categorized into one of the following bins:

| Category | Description                                          |
| -------- | ---------------------------------------------------- |
| 0        | No Detail (e.g. CEIAS record only)                   |
| 1        | Symbolic (e.g. cultural, ceremonial)                 |
| 2        | Economic/Diplomatic (e.g. trade talks, MoUs)         |
| 3        | Strategic (e.g. defense pacts, multilateral summits) |

---

Visualizations

Interactive Tableau dashboards were created to visualize:

* Visit frequency by year
* Visit intensity by country category
* Engagement type distribution

Live Dashboards:

* [Dashboard 1](https://public.tableau.com/app/profile/tanushree.jain6697/viz/Book1_17468069211000/Dashboard1?publish=yes)
* [Dashboard 2](https://public.tableau.com/app/profile/tanushree.jain6697/viz/Book1_17468069211000/Dashboard2?publish=yes)



Highlights

* Applied zero-shot NLP on visit summaries to infer purpose
* Automated batch classification using GPU
* Visual design inspired by CEIAS dashboard and Mapping Global China aesthetics

---

Technologies Used

* Python (Pandas, BeautifulSoup, Selenium)
* Hugging Face Transformers (Facebook BART)
* Tableau
* Jupyter Notebooks
