# leexi-saas-analysis

Technical case – SaaS revenue, churn and product usage analysis.

## Contexte

Ce projet a été réalisé dans le cadre d’un cas technique pour un stage de Data Analyst chez Leexi.

L’objectif est d’analyser un dataset SaaS afin de mieux comprendre :

- l’évolution du revenu récurrent mensuel (MRR) ;
- le churn client ;
- les différences de churn selon certains segments ;
- l’usage produit ;
- les KPIs pertinents pour piloter l’activité.

L’analyse complète, avec le code, les graphiques, les hypothèses et les limites, est disponible dans le notebook :

`Leexi_SaaS_Analysis_Maxim_Vicente.ipynb`

## Principales conclusions

- Le MRR augmente fortement sur la période étudiée.
- Le churn varie davantage selon le secteur d’activité et le canal d’acquisition que selon le niveau de plan.
- Le segment `DevTools` présente le taux de churn le plus élevé, autour de 31 %.
- Les comptes acquis via le canal `event` présentent un churn plus élevé que ceux provenant du canal `partner`.
- Les trois plans ont des taux de churn très proches, autour de 22 %.
- L’analyse de l’usage produit ne met pas en évidence de différence forte entre les comptes churnés et les comptes conservés.

## KPIs recommandés

Les principaux KPIs que je proposerais pour un dashboard SaaS sont :

- MRR total ;
- Nouveau MRR, MRR churné et évolution nette ;
- Taux de churn client ;
- Taux de churn du revenu ;
- Indicateur d’engagement produit.

## Hypothèses et limites

Plusieurs limites ont été identifiées dans les données :

- certaines valeurs manquantes ont une signification métier et ne sont donc pas nécessairement des erreurs ;
- `usage_id` contient quelques doublons ;
- une part importante des événements d’usage se situe en dehors de la période de validité de l’abonnement associé ;
- le churn existe à plusieurs niveaux : compte, abonnement et événement ;
- les données d’usage sont donc principalement exploitées de manière agrégée plutôt que temporelle.

Les résultats doivent être interprétés comme des analyses descriptives. Ils permettent d’identifier des tendances et des segments à surveiller, mais ne permettent pas à eux seuls d’établir des relations causales.

## Structure du projet

- `Leexi_SaaS_Analysis_Maxim_Vicente.ipynb` : notebook contenant l’ensemble de l’analyse, les visualisations et les conclusions.
- `README.md` : résumé du projet et des principaux résultats.
