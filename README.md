# CS-13 Capstone — Bird Breeding Analysis (Atlas + DES)

Combined NSW Bird Atlas and DES backlog breeding data, the team's Week 9 analysis, and a client-facing
insights notebook built around five research questions on preventing species decline.

## Layout

| Path | What it is |
|---|---|
| `combined_atlas_des.parquet` | Combined dataset, one row per species per survey sheet (see `README_combined_data.txt`) |
| `client_insights/Bird_Breeding_Insights.ipynb` | Five research questions → answer via visual; also builds the client PDF |
| `client_insights/outputs/` | Generated PDF report, chart PNGs and result tables (CSV) |
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

## Data handling

This repository contains client data and should stay **private**.
