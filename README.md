# Class D – Team 01 final project archive

CISC7204 Data Science and Data Visualization, 2026/2027 Semester 1.
Inbound tourism and electronic payment activity in Macao's restaurant sector.

This zip is `cisc7204-Class_D-Team_01-FinalProjectArchive.zip`. Unzip it and you should see this folder.

## What is in the folder

- `README.md` — this file.
- `codebook.md` — what each column means, and what the payment series is not.
- `requirements.txt` — the Python packages the notebook imports.
- `data/` — the DSEC files and a short note, `DATASETS.md`. The news text is the source of the monthly levels. The two Excel workbooks are the September 2026 releases, kept so a reader can see why they were not used as the time series.
- `notebooks/cisc7204_Class_D_Team_01_analysis.ipynb` — builds the 21-month table, draws Figures 1–6, fits the regression, and runs the checks named in the proposal.
- `visuals/` — the six figures written by the notebook.

## How to run it

From this folder, on macOS or Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/cisc7204_Class_D_Team_01_analysis.ipynb
```

In Jupyter, use Kernel → Restart & Run All. The notebook looks for `data/` in the folder above `notebooks/`. Do not move the notebook out of `notebooks/` unless you also move `data/`.

The script does not download anything. It does not need a DSEC login. It reads the files already in `data/`.

After a full run, `data/merged_monthly.csv` and the six PNG files in `visuals/` are rewritten. The numbers in the final report were taken from that run.

## What a correct run should show

- 21 months, January 2025 through September 2026, and no gap.
- January 2025 payment equal to 1.30 (MOP billion), the revised figure.
- Same-day plus overnight agreeing with the total used, within 5 persons, in every month.
- Pearson correlations in levels about 0.81 (same-day) and 0.73 (overnight).
- The two-predictor fit: same-day slope about 0.15, overnight slope about 0.08, with the overnight 95% interval crossing zero.

Team: CHEN RUXIN (MC65209), GUO JINZHENG (MC65088), CHAN CHENG I (MC64935), SUN JIA (MC65187), BAI HAOCHENG (MC65186), XIE ZIQI (MC65164).
