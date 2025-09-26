# Mapping Russian Prose

Companion repository for the CCLS 2025 study on **geocoding space in 19th-century Russian fiction**.

## Repository layout

```
mapping_russian_prose/
├─ code/                  # Analysis notebooks & environment
│  ├─ Geo Analysis for CCLS 2025.ipynb
│  └─ requirements.txt
│
├─ data/                  # Input data & resources
│  ├─ corpus metadata/    # Metadata tables for texts
│  │   ├─ realism_metadata.csv
│  │   └─ romantism_metadata.csv
│  │
│  ├─ geodata/            # Gazetteers & frequency tables
│  │   ├─ geo-coordinates-clean.json
│  │   ├─ realism-locations-freqs.tsv
│  │   └─ romantism-locations-freqs.tsv
│  │
│  └─ word2vec_models/    # Pretrained word2vec models (binary format)
│      ├─ word2vec_realism.model
│      └─ word2vec_romanticism.model
│
├─ figures/               # Exported figures for the paper
│  ├─ figure1.jpg
│  ├─ figure2.jpg
│  ├─ figure3.jpg
│  ├─ figure4.png
│  └─ figure5.png
│
└─ README.md
```

## Quick start

```bash
# 1) clone
git clone https://github.com/DanilSko/mapping_russian_prose.git
cd mapping_russian_prose

# 2) create & activate a virtual environment
python -m venv .venv
source .venv/bin/activate     # Windows: .venv\Scripts\activate

# 3) install dependencies
pip install -r code/requirements.txt

# 4) open the notebook
jupyter lab code/"Geo Analysis for CCLS 2025.ipynb"
```

## Data description

* **corpus metadata/**
  Work-level metadata tables for the corpus subsets:

  * `realism_metadata.csv`
  * `romantism_metadata.csv`

* **geodata/**
  Resources for geocoding and spatial frequency analysis:

  * `geo-coordinates-clean.json`: gazetteer of normalized place names with coordinates
  * `*_locations-freqs.tsv`: per-work frequency tables of toponyms

* **word2vec_models/**
  Pretrained distributional models trained on the two corpus subsets:

  * `word2vec_realism.model`
  * `word2vec_romanticism.model`

## Figures

All plots, maps, and visualizations generated during the analysis are stored in `figures/`. These correspond to the figures used in the CCLS 2025 paper.

## Citation

If you use this repository, please cite the associated CCLS 2025 paper:

```
@inproceedings{skorinkin_outward_2025,
	location = {Darmstadt},
	title = {The Outward Turn: Geocoding the Expansion of Fictional Space in Russian 19th Century Literature},
	rights = {{CC} {BY} 4.0 International - Creative Commons, Attribution},
	url = {https://tuprints.ulb.tu-darmstadt.de/30144/},
	shorttitle = {The Outward Turn},
	number = {1},
	institution = {Universitäts- und Landesbibliothek Darmstadt},
	author = {Skorinkin, Daniil and Orekhov, Boris},
	date = {2025-06-17},
	langid = {english},
	doi = {10.26083/tuprints-00030144},
	note = {Volume: 4},
}
```