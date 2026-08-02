# Quantitative Analyse von Abweichungen in Zahlungsprozessen

Dieses Repository enthält die Python-Notebooks der empirischen Analyse zur Bachelorarbeit. Tabellen und Abbildungen werden bei einer erneuten Ausführung im Ordner `outputs` erzeugt.

## Projektstruktur

```text
.
├── data_raw/
│   └── README.md
├── notebooks/
│   ├── 01_data_audit.ipynb
│   ├── 02_deviation_label_audit.ipynb
│   ├── 03_descriptive_process_analysis.ipynb
│   ├── 04_label_robustness_feature_availability.ipynb
│   ├── 05_prediction_design_baseline_modeling_v3_featuretypes_fixed_final.ipynb
│   ├── 06_prediction_refinement_ablation_timeprefixes.ipynb
│   ├── 07_benchmark_labels_inspection_case_selection.ipynb
│   ├── 08_benchmark_reconciliation_two_perspective_deep_dive.ipynb
│   ├── 09_comparative_prediction_final_robustness.ipynb
│   ├── 10_final_prediction_quality_closure_thesis_assets.ipynb
│   └── 11_heuristic_baselines_high_level_process_overview.ipynb
├── outputs/
│   └── README.md
├── .gitignore
└── requirements.txt
```

## Datensatz

Verwendet wird der **BPI Challenge 2018 Application Log**. Der Datensatz ist wegen seiner Dateigröße nicht Bestandteil des Repositorys. Nach dem Download muss die Datei unter folgendem Pfad liegen:

```text
data_raw/BPI_Challenge_2018.xes.gz
```

Die Downloadquelle und die Prüfsumme stehen in `data_raw/README.md`.

## Umgebung

Die Analyse wurde mit Python 3.11 durchgeführt. Unter Windows kann die Umgebung im Projektordner wie folgt eingerichtet werden:

```powershell
python -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Ausführung

Die Notebooks bauen teilweise auf zuvor erzeugten Dateien auf und werden deshalb in der Reihenfolge `01` bis `11` ausgeführt. Sie setzen den Ordner `notebooks` als Arbeitsverzeichnis voraus.

```powershell
cd notebooks
jupyter lab
```

Die Ergebnisdateien werden automatisch unter `outputs` angelegt und sind durch die `.gitignore` von der Versionsverwaltung ausgeschlossen.

## Datenquelle

Van Dongen, Boudewijn und Borchert, F. Florian (2018). *BPI Challenge 2018*. Version 1. 4TU.ResearchData. https://doi.org/10.4121/uuid:3301445f-95e8-4ff0-98a4-901f1f204972
