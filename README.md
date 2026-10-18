# CS-13 Capstone — Bird Breeding Analysis (Atlas + DES)

Combined NSW Bird Atlas and DES backlog breeding data, the team's Week 9 analysis, and a client-facing
insights notebook built around five research questions on preventing species decline.

## Layout

| Path | What it is |
|---|---|
| `combined_atlas_des.parquet` | Combined dataset, one row per species per survey sheet (see `README_combined_data.txt`) |
| `client_insights/Bird_Breeding_Insights.ipynb` | Five research questions → answer via visual; also builds the client PDF |
| `client_insights/outputs/` | Generated PDF report, chart PNGs and result tables (CSV) |
| `deeper_insights/Hidden_Pressures_Five_Questions.ipynb` | Five further questions: Noisy Miners, introduced birds, native winners and losers, migrants, priority breeding squares; also builds its own client PDF |
| `deeper_insights/outputs/` | `Hidden_Pressures_Report.pdf`, chart PNGs and result tables (CSV) |
| `decline_patterns/Q1_Continuing_Declines.ipynb` | Which species, if any, are continuing to decline; builds `outputs/Q1_Continuing_Declines.pdf` |
| `decline_patterns/Q2_Decline_Concentration.ipynb` | Whether declines are concentrated in particular regions, habitats or ecological groups; builds `outputs/Q2_Decline_Concentration.pdf` |
| `decline_patterns/species_traits_provisional.csv` | Provisional diet, habitat, nest, movement and size traits used by the Q2 notebook (check against the team trait table) |
| `decline_patterns/outputs/` | The two PDFs, chart PNGs and result tables (CSV) |
| `figures/`, `tables/` | Team's Week 9 figures and Excel tables |
| `Combined_Breeding_Analysis_Progress_Report_Section.docx` | Team's progress report section |
| `README.txt`, `README_combined_data.txt` | Data notes and agreed analysis rules |

## Running the notebook

```bash
pip install -r requirements.txt
jupyter notebook client_insights/Bird_Breeding_Insights.ipynb
```

Run all cells (about 20 seconds). Settings such as periods, thresholds and the report title are in the
**Settings you can customise** cell at the top; re-running regenerates every chart, sentence and
`client_insights/outputs/Bird_Breeding_Insights_Report.pdf`.

The second notebook runs the same way (about 45 seconds) and writes
`deeper_insights/outputs/Hidden_Pressures_Report.pdf`:

```bash
jupyter notebook deeper_insights/Hidden_Pressures_Five_Questions.ipynb
```

The two `decline_patterns` notebooks (about 2 minutes each) write one PDF each to `decline_patterns/outputs/`:

```bash
jupyter notebook decline_patterns/Q1_Continuing_Declines.ipynb
jupyter notebook decline_patterns/Q2_Decline_Concentration.ipynb
```

## Data handling

This repository contains client data and should stay **private**.
