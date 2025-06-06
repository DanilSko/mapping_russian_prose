# Mapping Russian Prose — Data & Code  
Companion materials for the CCLS-2025 study  
*“The outward turn: geocoding space in 19-century Russian fiction”*

---

## 1  Repository layout

| Path | Contents | Size* |
|------|----------|-------|
| `code/` | Reproducible analysis environment | |
| &nbsp;&nbsp;└── `Geo Analysis for CCLS 2025.ipynb` | End-to-end Jupyter workflow (load corpus → resolve toponyms → analyse → plot) | 45 kB |
| &nbsp;&nbsp;└── `requirements.txt` | Minimal Python stack (pandas ≥ 2, folium, matplotlib, seaborn) | 32 B |
| `geodata/` | Cleaned geospatial tables | |
| &nbsp;&nbsp;└── `geo-coordinates-clean.json` | Gazetteer: 6 k + toponyms with WGS-84 lat/long | 380 kB |
| &nbsp;&nbsp;└── `romantism-locations-freqs.tsv` | Romanticism corpus: toponym × text frequency matrix | 118 kB |
| &nbsp;&nbsp;└── `realism-locations-freqs.tsv` | Realism corpus: toponym × text frequency matrix | 525 kB |
| `romantism_metadata.csv` | Title, author, year for every Romanticism text | 7 kB |
| `realism_metadata.csv` | Same for Realism texts | 26 kB |
| `README.md` | ▸ *this file* | — |

\*Sizes are approximate for a fresh clone.

---

## 2  Quick start

```bash
# 1  clone
git clone https://github.com/<your-user>/mapping_russian_prose.git
cd mapping_russian_prose

# 2  create an isolated env (conda or venv)
python -m venv .venv
source .venv/bin/activate          # or .venv\Scripts\activate on Windows
pip install -r code/requirements.txt

# 3  run the analysis
jupyter lab code/Geo\ Analysis\ for\ CCLS\ 2025.ipynb
