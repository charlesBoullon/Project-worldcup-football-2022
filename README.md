# Analyse et Prédiction Coupe du Monde FIFA 2022

Ce notebook propose une analyse complète des données de la Coupe du Monde de la FIFA 2022, incluant extraction, nettoyage, visualisation et prédiction des résultats des matchs.

## Structure du notebook

1. **Extraction des données**
   - Récupération des groupes et résultats depuis Wikipedia (web scraping avec `pandas`, `BeautifulSoup`, `selenium`).
   - Sauvegarde des données extraites au format CSV et pickle.

2. **Nettoyage et transformation**
   - Nettoyage des données historiques et des fixtures.
   - Fusion et déduplication des datasets.
   - Transformation des scores, création de nouvelles colonnes (buts, total de buts, etc.).

3. **Visualisation**
   - Analyse des joueurs (dataset FIFA 22).
   - Visualisation des distributions de notes, meilleurs joueurs par équipe, etc. (avec `seaborn` et `matplotlib`).

4. **Prédiction**
   - Calcul de la force des équipes à partir des données historiques.
   - Modélisation des scores attendus avec la loi de Poisson (`scipy.stats.poisson`).
   - Simulation de la phase de groupes et des phases finales pour prédire les résultats.

## Fichiers générés

- `dict_table` : Dictionnaire des groupes et classements.
- `fifa_worldcup_historical_data.csv` : Données historiques des matchs.
- `fifa_worldcup_missing_data.csv` : Données manquantes récupérées.
- `clean_fifa_worldcup_matches.csv` : Données nettoyées et prêtes pour l'analyse.
- `clean_fifa_worldcup_fixture.csv` : Fixtures nettoyées.
- Visualisations et tableaux intermédiaires.

## Dépendances

- Python 3.x
- pandas
- numpy
- seaborn
- matplotlib
- bs4 (BeautifulSoup)
- requests
- selenium
- webdriver_manager
- scipy

## Utilisation

1. Installe les dépendances nécessaires :
    ```sh
    pip install pandas numpy seaborn matplotlib bs4 requests selenium webdriver_manager scipy
    ```

2. Lance le notebook dans Jupyter ou VS Code.

3. Exécute chaque cellule dans l'ordre pour reproduire l'analyse et la prédiction.

## Remarques

- Le scraping utilise des archives web pour garantir la reproductibilité.
- Certaines étapes nécessitent un navigateur Chrome installé pour Selenium.
- Les prédictions sont basées sur des statistiques historiques et la loi de Poisson.

---

N'hésite pas à adapter ce README selon tes besoins spécifiques !
