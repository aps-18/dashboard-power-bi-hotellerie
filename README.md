
# Tableau de bord Power BI — Hôtel Prestige

Projet réalisé dans le cadre du cours de Power BI encadré par Andre Angwe, en Master 1 Économétrie Appliquée à l'IAE Nantes.

L'objectif du projet était de concevoir un **tableau de bord décisionnel interactif** permettant d'analyser les performances financières, opérationnelles et commerciales d'un établissement hôtelier fictif.

Le projet mobilise l'ensemble de la chaîne de création d'un reporting Power BI : préparation des données avec Power Query, modélisation relationnelle, création d'indicateurs en DAX et conception de visualisations interactives.

## Contexte

Pour ce projet, nous avons imaginé **L'Hôtel Prestige**, un établissement fictif de luxe situé à Paris.

Son concept repose sur différents étages thématiques représentant plusieurs pays. Les chambres sont associées à des villes et réparties en trois catégories : Standard, Deluxe et Suite.

Le jeu de données a été généré spécifiquement pour simuler l'activité de cet établissement sur la période **2019-2024**. Il comprend notamment des informations relatives :

- aux réservations ;
- aux chambres ;
- aux clients ;
- aux prix et au chiffre d'affaires ;
- aux coûts opérationnels ;
- aux dépenses de restaurant et de spa ;
- aux canaux de réservation.

Les données sont fictives et ont été créées à des fins pédagogiques.

## Préparation et modélisation des données

Les données ont d'abord été préparées avec **Power Query** : correction des formats, transformations de variables, ajout de colonnes nécessaires aux analyses et actualisation des différentes sources.

Une **table Calendrier** a également été créée afin de permettre les analyses temporelles par année, trimestre, mois, semaine et saison.

Le modèle Power BI repose sur une **architecture en étoile**, avec :

- 2 tables de faits : réservations et coûts ;
- plusieurs tables de dimensions : pays/étages, villes/chambres et clients ;
- une table Calendrier ;
- une table dédiée aux mesures.

Cette organisation permet de relier les différentes dimensions de l'activité de l'hôtel tout en conservant un modèle lisible et adapté à l'analyse décisionnelle.

## Indicateurs et DAX

Plus de **50 mesures DAX** ont été construites afin de produire des indicateurs dynamiques s'adaptant aux filtres du tableau de bord.

Parmi les principaux KPI :

- chiffre d'affaires ;
- profit ;
- marge opérationnelle ;
- taux d'occupation ;
- prix moyen par nuit ;
- RevPAR ;
- taux d'annulation ;
- taux de no-show ;
- délai moyen entre réservation et séjour ;
- taux de fidélité ;
- chiffre d'affaires cumulé YTD ;
- croissance du chiffre d'affaires.

Des mesures spécifiques ont également été développées pour les analyses temporelles et la mise en forme dynamique des visualisations.

## Tableau de bord

Le tableau de bord est composé de **six pages complémentaires**, permettant de passer d'une vision générale de l'établissement à des analyses plus détaillées.

### 1. Accueil

Page d'introduction présentant l'identité visuelle de l'Hôtel Prestige et donnant accès aux différentes parties du tableau de bord.

![Accueil](dashboard/01_accueil.jpeg)

### 2. Performance globale

Cette page synthétise les principaux indicateurs financiers et opérationnels de l'établissement : chiffre d'affaires, profit, marge, prix moyen, taux d'occupation et taux d'annulation.

Elle permet également d'analyser la structure du chiffre d'affaires et la répartition des coûts opérationnels.

![Performance globale](dashboard/02_performance_globale.jpeg)

### 3. Performance par étages

Cette page compare les performances des différents étages thématiques de l'hôtel.

Elle permet notamment d'étudier le nombre de réservations, le chiffre d'affaires, la rentabilité et l'évolution du profit, ainsi que de mettre en relation **attractivité et rentabilité**.

![Performance par étages](dashboard/03_etages.jpeg)

### 4. Performance par type de chambre

Cette analyse porte sur les **300 chambres** de l'établissement et permet de comparer les catégories Standard, Deluxe et Suite.

Elle présente notamment le rendement par chambre, le tarif moyen, les coûts, le profit, la contribution au chiffre d'affaires et l'évolution du taux d'occupation.

![Performance par type de chambre](dashboard/04_chambres.jpeg)

### 5. Analyse client et demande

Cette page étudie le profil et le comportement de la clientèle.

Elle permet d'analyser :

- la contribution des différents types de clients au chiffre d'affaires ;
- la répartition de la clientèle ;
- l'origine géographique des clients ;
- les canaux de réservation ;
- le taux de fidélité ;
- les annulations et no-shows ;
- le délai moyen entre réservation et séjour.

![Analyse client et demande](dashboard/05_clients_demande.jpeg)

### 6. Analyse temporelle

La dernière page permet d'étudier l'évolution de l'activité sur la période **2019-2024**.

Elle regroupe notamment le chiffre d'affaires et le profit cumulés, la croissance du chiffre d'affaires, la marge opérationnelle, le taux d'occupation, l'évolution mensuelle de l'activité, le RevPAR et la structure des coûts.

![Analyse temporelle](dashboard/06_analyse_temporelle.jpeg)

## Interactivité

Le tableau de bord a été conçu pour permettre une exploration dynamique des données.

Les différentes pages comportent des filtres permettant notamment de sélectionner :

- l'année et le mois ;
- l'étage ;
- le type de chambre ;
- le type de client ;
- le canal de réservation.

Les visualisations interagissent également entre elles afin de permettre une analyse progressive des données.

## Technologies et compétences mobilisées

**Outil principal :** Power BI

**Préparation des données :**
- Power Query
- Excel
- Transformation et préparation des données

**Modélisation :**
- Modèle en étoile
- Tables de faits et de dimensions
- Table Calendrier
- Relations entre tables

**Analyse :**
- DAX
- Création de KPI
- Analyse financière et opérationnelle
- Analyse temporelle
- Segmentation de la clientèle

**Data visualisation :**
- Conception de tableaux de bord
- Visualisations interactives
- Filtres et segments
- Mise en forme conditionnelle
- Reporting décisionnel

## Structure du dépôt

```text
dashboard-power-bi-hotellerie/
├── README.md
├── dashboard/
│   ├── 01_accueil.jpeg
│   ├── 02_performance_globale.jpeg
│   ├── 03_etages.jpeg
│   ├── 04_chambres.jpeg
│   ├── 05_clients_demande.jpeg
│   └── 06_analyse_temporelle.jpeg
├── data/
│   └── db.xlsx
├── power-bi/
│   └── PowerBI_hotel.pbix
└── rapport/
    └── synthese.pdf
```

## Fichiers du projet

Le fichier Power BI complet est disponible dans le dossier [`power-bi`](power-bi/).

La synthèse détaillant la démarche, la construction du tableau de bord et l'interprétation des résultats est disponible ici :

[Consulter la synthèse du projet](rapport/synthese.pdf)

## Auteurs

- **Amélie Pires**
- Ikram Abouzayd
  
Master 1 Économétrie Appliquée — Power Bi — IAE Nantes, 2025-2026

## Contact

**Amélie Pires**

Mail : [amelie.pires@hotmail.com](mailto:amelie.pires@hotmail.com) · [LinkedIn](https://www.linkedin.com/in/amelie-pires) · [GitHub](https://github.com/aps-18)
