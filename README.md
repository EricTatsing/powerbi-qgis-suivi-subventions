# Piloter les aides régionales à l'économie circulaire avec Power BI et QGIS

Conception des premiers tableaux de bord du Service Déchets & Économie Circulaire de la Région Nouvelle-Aquitaine, et cartographie des aides à l'échelle des départements et des intercommunalités.

> Stage de 6 mois, Région Nouvelle-Aquitaine (Bordeaux). Les captures sont anonymisées : les noms de bénéficiaires et les montants individuels sont masqués.

## Le besoin
Le suivi des subventions était dispersé dans une vingtaine de fichiers Excel (environ 1 000 porteurs de projets). Le service n'avait aucune vue d'ensemble pour répondre à des questions simples : combien a-t-on engagé et payé, sur quels territoires, pour quelles filières ?

## Ce que j'ai construit

### 1. Une base fiable
- Consolidation des fichiers en une base unique, automatisée en Python
- Dédoublonnage des projets et attribution d'un identifiant unique
- Rattachement de chaque projet à son intercommunalité (EPCI), à partir du référentiel officiel INSEE / DGCL

### 2. Un modèle de données en étoile
Une table de faits (les lignes de subventions) reliée à des dimensions : dates, filières, porteurs, territoires. Environ 30 mesures DAX : montants engagés et payés, taux de paiement, nombre de projets, aide par habitant, évolution sur un an.

![Modèle de données](modele_etoile.png)

### 3. Les tableaux de bord
**Synthèse** : Confidentiel

![Synthèse](dashboard_synthese.png)

**Territoires** : Confidentiel

![Territoires](dashboard_territoires.png)

### 4. La cartographie QGIS
Cartes choroplèthes des aides par département et par EPCI, réalisées à partir des données du tableau de bord.

![Aides par département](carte_aides_departements.png)

![Aides par EPCI](carte_epci.png)

## Utilisation
Les fiches départementales et le suivi des subventions ont été présentés lors d'une conférence territoriale dans les Landes, pour trois départements (Landes, Lot-et-Garonne, Pyrénées-Atlantiques).

**Outils :** Power BI · DAX · Power Query · QGIS · Python (pandas) · modélisation en étoile
