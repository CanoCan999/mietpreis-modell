# Mietpreis-Modell NRW

Ein Jupyter-Notebook, das öffentliche Mietinserate lädt, bereinigt und mit **scikit-learn** ein Modell zur Vorhersage der Kaltmiete trainiert.

## Daten

[Apartment rental offers in Germany](https://www.kaggle.com/datasets/corrieaar/apartment-rental-offers-in-germany) auf Kaggle (Inserate von ImmobilienScout24).
Verwendet werden nur Wohnungen aus Nordrhein-Westfalen.

Der Datensatz ist nicht im Repository enthalten. Zum Ausführen `immo_data.csv` von Kaggle herunterladen und in diesen Ordner legen.

## Vorgehen

1. Daten laden und auf NRW filtern
2. Explorative Analyse (Verteilungen, fehlende Werte, Fläche vs. Miete)
3. Bereinigung (Plausibilitätsgrenzen, Ausreißer, Datentypen)
4. Feature-Vorbereitung mit `ColumnTransformer` (Median-Imputation, One-Hot-Encoding)
5. Train/Test-Split 80/20
6. Modelle: Lineare Regression (Baseline) und Random Forest
7. Auswertung mit MAE und R², Feature Importance
8. Fazit und Verbesserungsideen

## Ergebnisse

| Modell | MAE (€) | R² |
|---|---|---|
| Naiv (Durchschnitt) | 247.20 | 0,00 |
| Lineare Regression | 106.06 | 0.81 |
| Random Forest | 82.15 | 0.86 |

## Ausführen

```bash
pip install -r requirements.txt
jupyter notebook mietpreis_modell.ipynb
```

## Autor

Can Coskun
