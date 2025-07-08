
# Mapping China's Diplomatic Visits – Code Documentation

This repository contains the code used to extract, clean, merge, classify, and visualize data on China's diplomatic visits. The analysis is part of the "Mapping Global China" project.

## Code File Overview and Execution Order

To understand and reproduce the analysis, follow the notebooks in the order listed below:


### 1. `FromWikipedia.ipynb`
**Purpose**: Scrapes diplomatic visit data from [Wikipedia](https://en.wikipedia.org/wiki/List_of_international_trips_made_by_Xi_Jinping).

- Extracts data on trips made by Xi Jinping.
- Captures details like date, country, and purpose.
- Outputs a preliminary CSV of trip data.

---

### 2. `DataFromMFA.ipynb`
**Purpose**: Parses data from China’s Ministry of Foreign Affairs (MFA).

- Extracts and structures information from JSON/HTML-like content.
- Adds leader names, countries, and visit context.
- Includes additional trips by other top leaders like Li Keqiang and Li Qiang.

---

### 3. `MergingDatasets.ipynb`
**Purpose**: Combines data from multiple sources (Wikipedia, MFA, CEIAS) into a single clean dataset.

- Removes duplicates and harmonizes date formats.
- Standardizes country names and aligns categories.
- Adds continent and development status metadata.

---

### 4.  `FinalClassification.ipynb`
**Purpose**: Applies Natural Language Processing (NLP) to classify the intent of each diplomatic visit.

- Uses Facebook’s BART model for zero-shot classification via Hugging Face.
- Categories:
  - 0 = No detail
  - 1 = Symbolic (e.g., cultural)
  - 2 = Economic/Diplomatic (e.g., trade deals)
  - 3 = Strategic (e.g., military alliances)
- Outputs a final CSV with classification scores.

---

## Dependencies

- Python 3.7+
- `pandas`, `numpy`
- `beautifulsoup4`, `selenium`, `requests`
- `transformers` (Hugging Face)
- `sklearn`, `matplotlib`, `seaborn`

(Use `pip install -r requirements.txt` if a list is provided.)


## Suggested Reading Flow

1. `FromWikipedia.ipynb`
2. `DataFromMFA.ipynb`
3. `MergingDatasets.ipynb`
4. `FinalClassification.ipynb`



---

"""

with open("/mnt/data/README_CODE_ONLY.md", "w") as f:
    f.write(readme_content)

"README_CODE_ONLY.md"


