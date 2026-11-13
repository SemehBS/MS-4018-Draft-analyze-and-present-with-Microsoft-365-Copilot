# MS-4018 — TP Copilot dans Excel : Retail360

> **Durée obligatoire : 30 minutes** · Niveau débutant/intermédiaire · Scénario : ventes multicanales de produits divers · Version : 1.0 · Langue : français

## 1. Alignement avec le cahier des charges

Le document client *Unlocking Productivity with M365 Copilot Premium*, page 2, attribue **30 minutes** à « Copilot in Excel » dans un cursus de 2 heures. La page 4 décrit quatre objectifs : (1) questions en langage naturel et génération de colonnes calculées ; (2) tendances, insights, graphiques et tableaux croisés dynamiques ; (3) révision des suggestions, surlignage, tri et filtre ; (4) formule expliquée pas à pas et analyse de bout en bout. Le scénario Retail360 est une **proposition pédagogique créée pour satisfaire ces objectifs** : il ne figure pas dans le PDF du client.

**Résultat visé :** transformer un export brut de commandes en diagnostic commercial vérifiable, avec des formules, des segments de vente, un graphique et trois recommandations pour la direction.

## 2. Contexte métier et mission

Retail360 vend des ordinateurs, écrans, accessoires, mobilier, fournitures et équipements électroniques en France. Les commandes proviennent de boutiques, du commerce en ligne et de revendeurs. Vous êtes analyste commercial. Votre directrice des ventes demande : « Quel chiffre d'affaires avons-nous réalisé en 2025 ? Quels produits, régions et canaux tirent les ventes ? Les remises dégradent-elles nos marges ? Préparez une synthèse factuelle et un graphique. »

**Convention essentielle :** seules les commandes `Livrée` contribuent au chiffre d'affaires net et à la marge réalisée ; `Annulée` et `Retournée` sont exclues. Le chiffre d'affaires est **HT après remise**, pas le montant brut avant remise. Le coût des produits est pris en compte uniquement sur les unités livrées. Il s'agit de données fictives.

## 3. Fichiers fournis

- `ventes_retail360_2025.csv` : **600 lignes**, 14 colonnes, données propres pour le parcours de 30 minutes ; séparateur `;`, UTF-8 avec BOM, dates ISO `AAAA-MM-JJ`, décimales avec point dans le fichier CSV.
- `ventes_retail360_2025_qualite.csv` : **601 lignes**, variante pour l'atelier bonus sur la qualité ; anomalies volontaires : casse incohérente d'une région, remise aberrante à 85 %, quantité nulle, nom de produit manquant et ID dupliqué. Ne pas utiliser pour les résultats de référence du TP principal.

### Dictionnaire de données

| Colonne | Sens | Exemple / remarque |
|---|---|---|
| ID_Commande | Identifiant de commande | CMD-0001 ; unique dans le fichier principal |
| Date_Commande | Date de la vente | 2025-01-15 ; convertir en date Excel |
| ID_Produit | Référence | P001 à P012 |
| Produit | Libellé commercial | Écran 27 pouces |
| Categorie | Famille de produits | Informatique, Accessoires, Mobilier, Électronique, Fournitures |
| Region | Zone géographique | Nord, Sud, Est, Ouest, Île-de-France |
| Canal | Origine commerciale | Boutique, E-commerce, Revendeur |
| Commercial | Responsable | Six commerciaux fictifs |
| Type_Client | Segment de clientèle | Entreprise, Particulier, Administration |
| Quantite | Nombre d'unités | Entier |
| Prix_Unitaire_HT | Prix HT avant remise | EUR par unité |
| Remise_Pct | Taux de remise | 0,05 = 5 % |
| Cout_Unitaire_HT | Coût unitaire HT | EUR par unité |
| Statut | État de commande | Livrée, Retournée, Annulée |

### Préparation technique par le formateur (avant la session)

1. Vérifier que chaque participant dispose d'une licence **Microsoft 365 Copilot éligible à Copilot dans Excel**, d'une version d'Excel compatible et d'un accès OneDrive ou SharePoint selon la configuration de l'organisation.
2. Déposer le CSV principal dans un espace partagé et préparer un classeur Excel `.xlsx` enregistré dans OneDrive/SharePoint si l'environnement l'exige. Éviter de rester sur le CSV : les formules, graphiques et tableaux doivent être conservés dans le `.xlsx`.
3. Dans Excel, importer via **Données > À partir d'un fichier texte/CSV** ; vérifier le délimiteur point-virgule, la conversion des dates et des nombres, puis **Charger**. Adapter les paramètres régionaux d'import si nécessaire.
4. Cliquer dans la plage, **Insertion > Tableau**, cocher « Mon tableau comporte des en-têtes » et nommer le tableau `Ventes` dans l'onglet **Création de tableau**.
5. Enregistrer sous `Retail360_Analyse_Copilot.xlsx`. Vérifier que le bouton Copilot est accessible et que le tableau est reconnu. Les fonctions, boutons et capacités exacts varient selon le canal, la licence et la version d'Excel ; préparer un plan B manuel.
6. Ne jamais utiliser de données clients réelles pour ce TP. Vérifier le contexte de partage et les permissions avant de demander une analyse à Copilot.

## 4. Déroulé chronométré — 30 minutes exactement

| Temps | Durée | Manipulation principale | Livrable observable |
|---|---:|---|---|
| 00:00–03:00 | 3 min | Ouvrir le classeur, contrôler le tableau `Ventes`, repérer les champs | Source exploitable |
| 03:00–07:00 | 4 min | Interroger Copilot sur structure, statuts et qualité | Compréhension du dataset |
| 07:00–13:00 | 6 min | Faire proposer, expliquer, vérifier et appliquer des colonnes de formules | CA et marge calculés |
| 13:00–18:00 | 5 min | Explorer KPI, tendances, catégories et remises | 3 constats chiffrés |
| 18:00–23:00 | 5 min | Créer un TCD et un graphique avec Copilot ou le plan B | Synthèse visuelle |
| 23:00–27:00 | 4 min | Trier, filtrer, mettre en évidence et itérer | Vue des ventes à risque |
| 27:00–30:00 | 3 min | Vérifier les résultats et produire une synthèse de direction | 3 recommandations |

> **Animation :** faire démontrer chaque étape par le formateur (30–60 s), puis laisser les participants exécuter la manipulation. Si Copilot ne produit pas un objet Excel directement, le faire créer manuellement à partir des suggestions : l'objectif est de savoir **contrôler et appliquer** une réponse, pas de supposer que toute action est automatisée.

## 5. Guide pas à pas : parcours principal

### Étape 1 — Ouvrir et comprendre le tableau (00:00–03:00)

**Manipulations :** ouvrir le fichier `.xlsx` préparé ; vérifier les 600 commandes et 14 champs initiaux ; sélectionner une cellule du tableau `Ventes` ; repérer les colonnes `Statut`, `Quantite`, `Prix_Unitaire_HT`, `Remise_Pct` et `Cout_Unitaire_HT` ; ouvrir le volet Copilot. Montrer comment retrouver la source utilisée dans la réponse.

**Question d'amorce :** « Que représente une ligne ? Peut-on additionner toutes les commandes pour calculer les ventes réalisées ? » Réponse attendue : non, il faut exclure les statuts non livrés.

### Étape 2 — Poser des questions métier en langage naturel (03:00–07:00)

**Prompt A — reconnaissance du fichier**

```text
Tu es analyste des ventes. Analyse uniquement le tableau Excel nommé Ventes.
Décris en 5 points : le nombre de lignes, la période couverte, les catégories,
les canaux de vente et les valeurs distinctes du champ Statut.
Ne suppose aucune information absente du tableau. Signale les limites.
```

**Prompt B — cadrage du KPI**

```text
Dans Ventes, explique pourquoi le chiffre d'affaires réalisé ne doit pas
inclure les commandes Annulée et Retournée. Identifie précisément les colonnes
nécessaires pour calculer chiffre d'affaires HT net, coût et marge.
Présente la réponse sous forme de tableau : indicateur, colonnes, règle.
```

**Manipulations complémentaires :** reformuler « Quel est le meilleur produit ? » en « Quel produit a le CA HT net livré le plus élevé ? » ; demander les catégories les plus représentées ; demander les valeurs manquantes ; contrôler les nombres de lignes et les statuts via les filtres Excel.

**Contrôle :** la période doit être 2025 ; les trois statuts sont `Livrée`, `Retournée`, `Annulée`. Ne pas considérer une réponse narrative comme preuve de calcul.

### Étape 3 — Construire des formules et les expliquer (07:00–13:00)

**Prompt C — proposition de formules**

```text
Dans le tableau Ventes, propose les colonnes calculées suivantes :
1. CA_Net_HT : Quantite × Prix_Unitaire_HT × (1 − Remise_Pct),
   uniquement si Statut = "Livrée", sinon 0.
2. Cout_Total_HT : Quantite × Cout_Unitaire_HT si Livrée, sinon 0.
3. Marge_HT : CA_Net_HT − Cout_Total_HT.
4. Taux_Marge : Marge_HT / CA_Net_HT si CA_Net_HT > 0, sinon 0.
Explique chaque formule pas à pas, donne sa version Excel français avec
références structurées, et demande ma validation avant toute modification.
```

**Formules de référence (Excel en français ; séparateur `;`) :**

```excel
=SI([@Statut]="Livrée";[@Quantite]*[@Prix_Unitaire_HT]*(1-[@Remise_Pct]);0)
=SI([@Statut]="Livrée";[@Quantite]*[@Cout_Unitaire_HT];0)
=[@CA_Net_HT]-[@Cout_Total_HT]
=SI([@CA_Net_HT]>0;[@Marge_HT]/[@CA_Net_HT];0)
```

**Manipulations :** lire les formules proposées ; vérifier les conditions sur `Statut` ; demander à Copilot d'expliquer la remise de 10 % sur une commande de deux unités ; accepter les suggestions si elles sont correctes ; sinon créer les quatre colonnes à droite du tableau et saisir les formules ; formater `CA_Net_HT`, `Cout_Total_HT`, `Marge_HT` en devise EUR et `Taux_Marge` en pourcentage. Contrôler une ligne `Livrée` et une ligne `Annulée`.

**Prompt D — correction / itération**

```text
Ta proposition doit exclure les commandes Retournée et Annulée du chiffre
d'affaires et de la marge. Corrige les formules sans modifier les données
sources. Explique en une phrase la différence entre marge en euros et taux de marge.
```

**Piège pédagogique :** `Marge_HT / CA_Net_HT` correspond ici au **taux de marge sur chiffre d'affaires**, souvent appelé **taux de marque** dans le vocabulaire commercial français. Pour éviter l'ambiguïté, renommer idéalement cette colonne `Taux_Marge_sur_CA` ; la formule ne représente pas `Marge / Coût`.

### Étape 4 — Analyser la performance (13:00–18:00)

**Prompt E — diagnostic chiffré**

```text
À partir du tableau Ventes et des colonnes calculées, considère uniquement
les ventes Livrée. Calcule le chiffre d'affaires HT net, la marge HT et le
taux de marge sur CA global (somme des marges / somme des CA).
Présente ensuite les 5 catégories classées par CA, les 3 canaux et les
5 régions. Pour chaque segment : CA, marge, taux de marge sur CA.
Précise les critères de calcul et ne mélange pas moyenne des taux et taux global.
```

**Prompt F — tendances et anomalies**

```text
Analyse l'évolution mensuelle du CA_Net_HT des ventes Livrée en 2025.
Identifie le meilleur et le moins bon mois, la tendance générale et deux
hypothèses à investiguer. Distingue clairement faits observés et hypothèses.
Compare aussi les remises accordées par canal sans affirmer de causalité.
```

**Manipulations :** demander « top 5 produits par CA » ; « top 5 par marge » ; « régions sous le taux de marge global » ; « impact des remises » ; « CA par type de client ». Vérifier le classement par un tri ou un TCD. Ne pas confondre volume, CA et rentabilité.

### Étape 5 — Tableau croisé dynamique et graphique (18:00–23:00)

**Prompt G — TCD**

```text
Propose un tableau croisé dynamique à partir de Ventes, filtré sur Statut = Livrée.
Lignes : Categorie. Colonnes : Canal. Valeurs : somme de CA_Net_HT et somme
de Marge_HT. Indique les étapes exactes de construction et les erreurs à éviter.
Si tu peux créer le TCD dans Excel, propose de le faire dans une nouvelle feuille
nommée Synthese_Categories, après confirmation.
```

**Manipulations / plan B manuel :** `Insertion > Tableau croisé dynamique` ; source `Ventes` ; nouvelle feuille ; placer `Categorie` en lignes, `Canal` en colonnes, `CA_Net_HT` et `Marge_HT` en valeurs (agrégation **Somme**), `Statut` en filtre puis choisir `Livrée`. Renommer la feuille `Synthese_Categories`. Vérifier que les totaux concordent avec les KPI.

**Prompt H — graphique**

```text
Propose un graphique en colonnes comparant le CA_Net_HT des catégories
pour les commandes Livrée. Donne un titre explicite, les unités en euros,
un ordre décroissant et une recommandation de lisibilité. Si possible,
crée le graphique à partir du tableau croisé dynamique après confirmation.
```

**Manipulations :** insérer un graphique en colonnes depuis le TCD ; renommer « Chiffre d'affaires HT net par catégorie — 2025 » ; vérifier les unités, les étiquettes et le filtre `Livrée`. Variante si temps : graphique en courbe du CA mensuel ; segment (slicer) `Canal` ; chronologie `Date_Commande`.

### Étape 6 — Filtrer, trier, surligner, améliorer (23:00–27:00)

**Prompt I — repérage des ventes à surveiller**

```text
Dans Ventes, aide-moi à repérer les commandes Livrée dont Remise_Pct
est supérieure ou égale à 15 % et dont Taux_Marge est inférieur à 20 %.
Propose un filtre, un tri par Marge_HT croissante et une mise en forme
conditionnelle des lignes concernées. Ne modifie rien sans ma validation.
```

**Manipulations :** filtrer `Statut = Livrée`, `Remise_Pct >= 15 %`, `Taux_Marge < 20 %` ; trier `Marge_HT` croissante ; surligner la colonne `Taux_Marge` avec une règle `Inférieur à 0,20` ; contrôler que la règle s'applique à la plage attendue ; effacer les filtres à la fin. Si la mise en forme conditionnelle n'est pas réalisable depuis Copilot, utiliser **Accueil > Mise en forme conditionnelle**.

**Prompt J — itération**

```text
Réduis le périmètre aux commandes Livrée du canal E-commerce.
Explique quels filtres sont actifs, combien de lignes restent visibles,
et pourquoi un faible taux de marge ne signifie pas automatiquement une perte.
```

### Étape 7 — Vérification et restitution (27:00–30:00)

**Prompt K — synthèse pour la direction**

```text
Rédige une synthèse de direction de 120 mots maximum fondée uniquement sur
le tableau Ventes. Donne 3 constats chiffrés vérifiables, 2 points de vigilance
et 3 actions commerciales concrètes. Pour chaque chiffre, précise le filtre
Statut = Livrée et la mesure utilisée. N'invente ni causalité ni prévision.
```

**Débrief :** un participant montre un KPI, un graphique et un filtre ; le groupe vérifie un résultat à l'aide d'Excel. Poser les questions : « Qu'a calculé Copilot ? », « Qu'avons-nous vérifié ? », « Quelle décision serait prématurée ? ».

## 6. Résultats de contrôle (fichier principal uniquement)

Ces chiffres proviennent du CSV principal généré avec une graine fixe, et permettent de contrôler la cohérence des manipulations :

| Mesure | Valeur attendue |
|---|---:|
| Nombre total de commandes | 600 |
| Nombre de commandes `Livrée` | 505 |
| CA HT net réalisé | **437 100,35 €** |
| Marge HT réalisée | **126 093,35 €** |
| Taux de marge sur CA global | **28,85 %** (arrondi) |

Le nombre de commandes non livrées est 95. **Attention :** un calcul qui additionne tous les statuts ou utilise le prix avant remise ne correspond pas à ces résultats. Les résultats peuvent différer si un participant travaille sur la variante « qualité », modifie les filtres ou importe incorrectement les décimales.

## 7. Banque de manipulations supplémentaires (hors des 30 minutes)

Chaque manipulation est optionnelle et peut devenir une micro-démonstration de 2 à 5 minutes. **Ne pas chercher à tout faire dans les 30 minutes contractuelles.**

### A. Exploration et compréhension

1. Demander le dictionnaire des colonnes et leur type présumé.
2. Détecter les colonnes numériques importées comme texte.
3. Rechercher valeurs vides, doublons d'ID et quantités nulles.
4. Compter les commandes par statut et par région.
5. Comparer le nombre de commandes aux unités vendues.
6. Identifier les dix plus grosses commandes livrées.
7. Déterminer le panier moyen des commandes livrées : CA / nombre de commandes livrées.
8. Distinguer moyenne simple de remise et remise pondérée par valeur brute.

### B. Formules et calculs

9. Créer `Montant_Brut_HT = Quantite * Prix_Unitaire_HT`.
10. Créer `Montant_Remise_HT = Montant_Brut_HT * Remise_Pct`.
11. Créer `CA_Net_HT` avec condition sur `Statut`.
12. Créer `Cout_Total_HT` avec condition sur `Statut`.
13. Créer `Marge_HT` et expliquer le signe négatif éventuel.
14. Créer `Taux_Marge_sur_CA` et le formater en %.
15. Créer `Annee = ANNEE([@Date_Commande])`.
16. Créer `Mois_Num = MOIS([@Date_Commande])` pour un tri chronologique fiable.
17. Créer `Mois = TEXTE([@Date_Commande];"mmmm")` et expliquer pourquoi le tri alphabétique est incorrect.
18. Créer `Trimestre = "T"&(ENT((MOIS([@Date_Commande])-1)/3)+1)` ; vérifier les parenthèses si Copilot propose une formule invalide.
19. Créer `Alerte_Remise = SI([@Remise_Pct]>=0,15;"Remise forte";"Standard")`.
20. Créer `Alerte_Marge = SI(ET([@Statut]="Livrée";[@Taux_Marge]<0,2);"À surveiller";"OK")`.
21. Comparer `SOMME.SI.ENS` et TCD pour obtenir le CA par canal.
22. Demander une explication cellule par cellule d'une formule structurée.
23. Corriger une formule proposée qui inclut les commandes retournées.
24. Comparer marge en euros, taux de marge sur CA et marge sur coût.

### C. Analyses commerciales

25. Top 5 produits par CA.
26. Top 5 produits par marge absolue.
27. Top 5 produits par unités vendues.
28. Catégorie la plus rentable en taux de marge sur CA.
29. Classement des régions par CA et par marge.
30. Performance des canaux Boutique / E-commerce / Revendeur.
31. Comparaison des segments Entreprise / Particulier / Administration.
32. CA et marge par commercial, sans conclure sur leur performance individuelle sans contexte.
33. Évolution mensuelle du CA, de la marge et du panier moyen.
34. Comparaison premier et second semestre.
35. Comparaison des trimestres et contribution au total annuel.
36. Analyse des remises par catégorie et par canal.
37. Nombre et valeur brute des commandes annulées/retournées, sans les assimiler à des ventes réalisées.
38. Sensibilité : simuler une réduction de remise de 2 points sur les ventes livrées, **sans** prétendre prévoir la demande.
39. Contribution cumulée des produits au CA (analyse Pareto).
40. Identifier les combinaisons catégorie/canal à faible marge.

### D. Visualisations et interactions Excel

41. TCD CA par catégorie et canal.
42. TCD marge par région et type de client.
43. TCD CA par mois et catégorie.
44. Graphique en colonnes des catégories.
45. Courbe mensuelle du CA.
46. Barres horizontales des dix meilleurs produits.
47. Graphique combiné CA + taux de marge (vérifier l'axe secondaire).
48. Segments `Region`, `Canal` et `Categorie` sur un TCD.
49. Chronologie sur `Date_Commande` si dates correctement reconnues.
50. Mise en forme conditionnelle des faibles marges.
51. Mise en évidence des remises élevées.
52. Tri multicritère région puis CA décroissant.
53. Filtrage des seules commandes livrées et e-commerce.
54. Dupliquer un graphique puis changer son axe pour illustrer les risques de mauvaise lecture.

### E. Esprit critique et gouvernance

55. Demander à Copilot de citer les colonnes à l'origine de chaque KPI.
56. Lui faire expliquer pourquoi `MOYENNE(Taux_Marge)` n'est pas le taux global.
57. Lui demander d'identifier les hypothèses non prouvées dans une synthèse.
58. Comparer un prompt vague et un prompt cadré (objectif, contexte, source, format).
59. Demander une proposition de modification **sans l'appliquer**, puis la relire.
60. Recalculer manuellement un échantillon de trois commandes.
61. Vérifier l'impact d'un filtre oublié sur le résultat.
62. Tester l'atelier qualité : doublon, remise 85 %, région `nord`, quantité 0, produit vide.
63. Demander un plan de nettoyage **non destructif** de la variante qualité.
64. Construire une synthèse distinguant observations, hypothèses et recommandations.

## 8. Prompts bonus prêts à copier-coller

### Prompt « Pareto produits »

```text
Sur les seules commandes Livrée de Ventes, classe les produits par CA_Net_HT
décroissant. Calcule leur part du CA total et leur part cumulée. Identifie
combien de produits représentent environ 80 % du CA. Explique les limites
d'une interprétation commerciale fondée uniquement sur le CA.
```

### Prompt « Analyse des remises »

```text
Pour chaque Canal, compare CA_Net_HT, Marge_HT, taux de marge sur CA et remise
moyenne sur les commandes Livrée. Indique clairement si la remise moyenne
est simple ou pondérée. N'affirme pas que les remises causent la baisse de marge.
```

### Prompt « Contrôle qualité »

```text
Analyse la variante de données qualité sans la modifier. Recherche :
identifiants de commande dupliqués, régions incohérentes, produits vides,
quantités nulles et remises supérieures à 50 %. Propose un tableau des
anomalies avec colonne, problème, impact métier et correction à valider.
```

### Prompt « Direction commerciale »

```text
Agis comme contrôleur de gestion. Rédige un rapport factuel de 150 mots
maximum avec : CA HT net réalisé, marge HT, taux de marge sur CA, catégorie
leader, canal leader, une anomalie à surveiller et trois actions. Chaque
affirmation chiffrée doit pouvoir être vérifiée dans le tableau Ventes.
```

### Prompt « Contre-expertise »

```text
Audite ta dernière réponse. Identifie les chiffres non sourcés, les erreurs
potentielles de filtres, les confusions entre montant brut et net, les moyennes
incorrectes et les conclusions causales non démontrées. Propose une version
corrigée et explique les vérifications que je dois faire dans Excel.
```

## 9. Variantes d'animation

**Version débutant (30 min) :** le formateur fournit un `.xlsx` déjà importé avec `Ventes` ; les participants réalisent les étapes 1 à 7. Priorité à la compréhension des résultats et à la validation des formules.

**Version intermédiaire (45–60 min) :** ajout de l'import CSV, de deux TCD, des segments, de la courbe mensuelle et d'un audit des remises.

**Version avancée (75–90 min) :** ajout de la variante qualité, d'un contrôle Pareto, de KPI pondérés, d'une analyse de sensibilité et d'une restitution argumentée.

**Démo formateur sans accès Copilot :** saisir les formules de référence, créer un TCD manuellement, puis présenter les prompts comme exemples de dialogue à tester ultérieurement. Ne pas présenter une fonctionnalité absente comme disponible.

## 10. Critères de réussite et grille d'évaluation

| Critère | Points | Preuve |
|---|---:|---|
| Formulation de prompts précis, ancrés sur `Ventes` | 2 | Prompts A/B/E |
| Formules correctes et exclusion des non-livrées | 3 | Colonnes calculées, contrôle de deux lignes |
| Interprétation des KPI et distinction CA/marge | 2 | CA, marge, taux global |
| TCD et graphique lisibles | 2 | Feuille de synthèse |
| Vérification critique d'une réponse Copilot | 1 | Correction documentée |
| **Total** | **10** | Réussite conseillée : 7/10 |

## 11. Dépannage rapide

| Symptôme | Vérification / solution |
|---|---|
| Copilot indisponible | Licence, application/version compatible, connexion, politique administrateur et emplacement du classeur ; utiliser le plan B manuel |
| Copilot ne reconnaît pas les données | Vérifier que la plage est un tableau structuré nommé `Ventes`, avec en-têtes uniques et sans cellules fusionnées |
| Les prix sont du texte | Réimporter le CSV en sélectionnant les paramètres régionaux adaptés au point décimal |
| Les dates sont du texte | Convertir `Date_Commande` en véritable date avant regroupement par mois |
| Formule refusée | Vérifier langue Excel, séparateurs `;` ou `,`, noms de fonctions et accents dans les valeurs de statut |
| TCD compte au lieu de sommer | Vérifier que `CA_Net_HT` est numérique ; choisir **Somme** dans les paramètres du champ |
| Résultat incohérent | Contrôler filtres, statut, remise et distinction entre somme des ratios et ratio des sommes |
| Copilot ne crée pas de TCD/graphique | Demander la procédure et exécuter l'insertion via le ruban Excel ; les capacités varient selon le déploiement |

## 12. Structure recommandée du dépôt GitHub

```text
ms4018-copilot-excel-retail360/
├── README.md                           # ce TP (renommer ce fichier)
├── data/
│   ├── ventes_retail360_2025.csv
│   └── ventes_retail360_2025_qualite.csv
├── exercices/
│   └── Retail360_Analyse_Copilot.xlsx  # créé par les participants
└── captures/                           # captures de démo, sans données sensibles
```

**Versionnement :** conserver les CSV en UTF-8, utiliser des commits distincts pour les changements de données et de prompts, ajouter une version du scénario en tête de document, et ne pas versionner de véritables données clients. Le fichier Excel final peut être ignoré par Git si les productions des participants sont personnelles.

## 13. Check-list formateur avant de démarrer

- [ ] Licence et Copilot dans Excel vérifiés sur le poste de démonstration.
- [ ] CSV principal importé correctement et classeur `.xlsx` sauvegardé.
- [ ] Tableau nommé `Ventes` et 600 lignes présentes.
- [ ] Colonnes de prix et de remise reconnues comme numériques.
- [ ] Statuts `Livrée`, `Retournée`, `Annulée` vérifiés.
- [ ] Contrôle du CA net et de la marge effectué avec les valeurs de référence.
- [ ] Plan B TCD/graphique manuel prêt.
- [ ] Chronomètre et objectifs des 30 minutes affichés.

---

**Source de cadrage :** document client *Unlocking Productivity with M365 Copilot Premium*, pages 2 (durées et prérequis) et 4 (Module 5 : Copilot in Excel). **Dataset, scénario, formules et prompts :** créations pédagogiques originales pour ce TP.
