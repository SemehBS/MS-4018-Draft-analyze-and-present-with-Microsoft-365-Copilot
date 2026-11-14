# TP MS-4018 — Créer et optimiser une présentation avec Copilot dans PowerPoint

> **Module :** Copilot dans PowerPoint · **Durée imposée :** 15 minutes · **Niveau :** débutant à intermédiaire  
> **Cas fil rouge :** Retail360 — bilan commercial 2025 et priorités 2026  
> **Livrable :** `Retail360_Bilan_Commercial_2025.pptx` (5 à 6 diapositives, avec notes)

## 1. Contexte et mission

Vous êtes responsable commercial de **Retail360**, une entreprise fictive qui vend des produits informatiques, électroniques, du mobilier, des accessoires et des fournitures. Vous venez de terminer une analyse des ventes 2025 dans Excel. La direction attend une présentation concise pour une réunion de pilotage : résultats clés, lecture des performances, risques et trois actions prioritaires pour 2026.

**Mission :** utiliser Microsoft 365 Copilot dans PowerPoint pour créer un premier support, l'améliorer, le réorganiser et le contrôler. L'enjeu n'est pas seulement de produire des diapositives : il faut conserver des chiffres exacts, des messages compréhensibles et des recommandations distinguant faits et hypothèses.

## 2. Objectifs pédagogiques

À l'issue du TP, le participant doit pouvoir :

1. Créer une présentation depuis une instruction ou un document Word de référence.
2. Obtenir un plan de diapositives adapté à un public de direction.
3. Ajouter ou retravailler une diapositive, son titre et son contenu.
4. Demander des notes du présentateur et une diapositive d'agenda.
5. Ajuster la mise en page et intégrer des visuels pertinents.
6. Résumer une présentation, en modifier l'ordre et vérifier les affirmations.
7. Identifier ce qui doit être effectué manuellement lorsque Copilot ne réalise pas une action.

## 3. Fichiers fournis et données de référence

Le TP s'appuie sur le cas Retail360 déjà utilisé dans Excel. Un document Word de briefing est fourni : `Brief_Retail360_Bilan_2025.docx`. Il contient le contexte, les chiffres validés et les consignes de restitution. Il peut servir de source pour la génération de diapositives **si cette fonction est disponible** dans l'environnement Microsoft 365. Une variante consiste à copier son contenu dans le prompt ou dans une présentation vierge.

### 3.1 Indicateurs validés

| Indicateur | Valeur de référence |
|---|---:|
| Commandes enregistrées en 2025 | 600 |
| Commandes livrées | 505 |
| Chiffre d'affaires net HT réalisé | 437 100,35 € |
| Marge HT réalisée | 126 093,35 € |
| Taux de marge sur CA global | 28,85 % (arrondi) |

**Règle métier :** les indicateurs de chiffre d'affaires et de marge réalisés portent uniquement sur les commandes au statut `Livrée`. Le taux global est le rapport *somme des marges / somme des CA*, et non la moyenne simple des taux par commande.

**Important :** aucune répartition chiffrée par produit, catégorie, région, canal ou mois n'est fournie dans le briefing. Copilot ne doit **pas inventer** de classement ni de tendance. Si vous disposez des résultats du TP Excel, vous pouvez les ajouter au document source après vérification.

### 3.2 Préparation du formateur (hors des 15 minutes)

- Vérifier la licence et l'accès à Copilot dans PowerPoint.
- Placer le document Word dans un emplacement OneDrive/SharePoint autorisé, si nécessaire.
- Préparer une présentation vierge et, si possible, un thème d'entreprise (couleurs, polices, logo fictif facultatif).
- Vérifier que les fonctionnalités « créer depuis un fichier », « modifier une diapositive » et « notes du présentateur » sont disponibles ; prévoir les variantes manuelles ci-dessous.
- Ne pas promettre une insertion automatique d'images, de graphiques ou de notes : la disponibilité dépend de l'application, de la licence et du déploiement.

## 4. Guide des fonctionnalités et de l'interface

Le TP combine **Copilot dans PowerPoint** et les **outils natifs de PowerPoint**. Les noms des commandes peuvent varier selon PowerPoint pour Windows, Mac ou le Web, ainsi que selon la licence et le déploiement. Le formateur teste les commandes dans son environnement avant la session.

| Fonctionnalité à explorer | Où agir | Ce que fait le participant | Nature |
|---|---|---|---|
| Volet Copilot | Bouton **Copilot** du ruban ou volet latéral | Ouvrir la conversation, saisir une demande, relancer et affiner | Copilot |
| Créer une présentation | Option de création avec Copilot, lorsqu'elle est proposée | Définir objectif, audience, longueur et source | Copilot |
| Créer depuis un document | Option **Créer à partir d'un fichier**, lorsqu'elle est proposée | Sélectionner le briefing Word accessible et contrôler les diapositives obtenues | Copilot, selon disponibilité |
| Ajouter une diapositive | Copilot ou **Accueil > Nouvelle diapositive** | Ajouter une diapositive de décisions, puis vérifier son emplacement | Copilot / natif |
| Réécrire une sélection | Sélectionner une zone de texte, puis utiliser Copilot si proposé | Raccourcir, reformuler, adapter le ton | Copilot, selon disponibilité |
| Synthétiser la présentation | Volet Copilot | Obtenir les messages clés et repérer les répétitions | Copilot |
| Générer des notes | Volet Copilot, puis volet **Notes** | Demander des notes orales, contrôler et insérer le résultat | Copilot / natif |
| Visuels et images | Copilot si option proposée ; **Insertion > Images / Icônes** | Ajouter un visuel pertinent et vérifier sa qualité | Copilot / natif |
| Suggestions de disposition | **Création > Concepteur / Suggestions de conception**, si disponible | Tester une disposition, puis comparer avant/après | Natif, éventuellement assisté |
| Thèmes et dispositions | **Création**, **Accueil > Disposition** | Appliquer une identité visuelle cohérente | Natif |
| Réorganisation | Volet des miniatures ou **Affichage > Trieuse de diapositives** | Déplacer et supprimer des diapositives | Natif ; Copilot peut conseiller |
| Accessibilité | **Révision > Vérifier l'accessibilité** (emplacement variable) | Contrôler contraste, ordre de lecture et texte alternatif | Natif |
| Présentation orale | **Diaporama**, mode Présentateur ; **Répéter avec le coach** si disponible | Tester le rythme, les notes et la durée | Natif |
| Export et diffusion | **Fichier > Exporter / Partager** | Enregistrer en PPTX ou exporter en PDF | Natif |

**Règle de démonstration :** ne pas annoncer qu'une modification a été effectuée tant qu'elle n'est pas visible sur la diapositive. Lorsque Copilot fournit seulement des conseils ou du texte, appliquer les changements dans PowerPoint.

## 5. Déroulé chronométré — 15 minutes

| Étape | Durée | Compétence | Preuve |
|---|---:|---|---|
| 1. Définir l'objectif et la source | 2 min | Prompt structuré et données fiables | Prompt initial |
| 2. Générer un premier support | 4 min | Création et agenda | 5 à 6 diapositives |
| 3. Enrichir et améliorer | 4 min | Reformulation, visuels, notes | 1 diapositive améliorée + notes |
| 4. Réorganiser et résumer | 3 min | Édition et synthèse | Ordre cohérent + résumé |
| 5. Contrôler et enregistrer | 2 min | Vérification critique | Fichier final et contrôle des KPI |
| **Total** | **15 min** | | |

### Étape 1 — Préparer la demande (0:00–2:00)

**Parcours guidé dans l'interface :**

1. Ouvrir PowerPoint et vérifier le compte Microsoft 365 connecté.
2. Ouvrir une présentation vierge, choisir un thème sobre dans **Création**, puis enregistrer le fichier sur un emplacement autorisé.
3. Cliquer sur **Copilot** pour ouvrir le volet conversationnel ; repérer la zone de saisie et les suggestions disponibles.
4. Ouvrir le briefing Word à côté de PowerPoint et identifier les cinq KPI de référence.
5. Expliquer aux participants la différence entre **demander un plan** et **demander la création effective des diapositives**.

**Manipulations :** ouvrir PowerPoint, créer une présentation vierge, ouvrir Copilot, vérifier que le briefing est accessible ou en copier le texte dans la conversation.

**Prompt 1 — Cadrer la présentation**

```text
Tu es responsable commercial chez Retail360. Je prépare un bilan 2025 pour
la direction, à présenter en 5 minutes. Propose un plan de 5 à 6 diapositives :
contexte, KPI, lecture des performances, points de vigilance, priorités 2026
et conclusion. Appuie-toi uniquement sur le document de briefing fourni.
Ne crée pas de chiffres manquants.
```

**À observer :** le plan est-il adapté à une direction ? Les titres expriment-ils une idée et non seulement un thème ? Les informations manquantes sont-elles signalées ?

### Étape 2 — Générer le premier support (2:00–6:00)

**Parcours guidé dans l'interface :**

1. Repérer l'option de création avec Copilot ; choisir la création à partir d'un fichier **si elle est affichée**.
2. Désigner `Brief_Retail360_Bilan_2025.docx` comme source, ou coller le contenu pertinent du briefing dans la demande.
3. Examiner le plan ou l'aperçu proposé : titres, ordre, nombre de diapositives et couverture des cinq KPI.
4. Confirmer la création, puis parcourir les diapositives via le volet des miniatures.
5. Ouvrir la diapositive des KPI et comparer chaque valeur au document Word.
6. Si l'agenda manque, demander à Copilot de l'ajouter ; sinon utiliser **Accueil > Nouvelle diapositive**, puis une disposition **Titre et contenu**.

**À montrer à l'écran :** la différence entre le contenu suggéré par Copilot et le contenu effectivement inséré dans la présentation.

**Manipulations :** utiliser la fonction de création depuis un fichier si disponible, sélectionner le briefing Word, ou générer à partir du prompt et du texte fourni. Examiner les diapositives avant toute validation.

**Prompt 2 — Générer la présentation**

```text
Crée une présentation professionnelle de 6 diapositives pour le comité de
direction de Retail360 à partir du briefing. Utilise un ton factuel, des
titres orientés message et peu de texte. Ajoute une diapositive d'agenda.
Présente les 5 KPI validés sans les modifier. Pour toute analyse non étayée,
indique « À confirmer avec l'analyse Excel ».
```

**Structure cible :**

1. Titre — Bilan commercial Retail360 2025.
2. Agenda — Résultats, constats, priorités.
3. Chiffres clés — 600 commandes, 505 livrées, 437 100,35 € de CA, 126 093,35 € de marge, 28,85 %.
4. Lecture commerciale — éléments démontrés, limites des données disponibles.
5. Priorités 2026 — trois actions proposées comme pistes à valider.
6. Conclusion — décisions attendues et prochaines analyses.

**Contrôle :** comparer les chiffres avec le tableau de référence ; ne pas confondre commandes enregistrées et commandes livrées.

### Étape 3 — Améliorer le fond et la forme (6:00–10:00)

**Parcours guidé dans l'interface :**

1. Sélectionner la diapositive des KPI et identifier un bloc trop dense.
2. Sélectionner le texte et utiliser l'option de réécriture Copilot **si proposée** ; sinon demander une reformulation dans le volet puis remplacer manuellement le texte.
3. Aller dans **Création > Concepteur / Suggestions de conception** si disponible ; comparer deux dispositions et conserver la plus lisible.
4. Utiliser **Accueil > Disposition** pour corriger la structure, et **Insertion > Icônes / Formes** pour créer des cartes KPI si nécessaire.
5. Demander à Copilot des notes du présentateur ; afficher **Notes** et vérifier qu'elles sont présentes, sinon les coller.
6. Tester l'ajout d'une image pertinente via Copilot **si disponible** ; sinon insérer une icône ou une image autorisée, puis vérifier le texte alternatif.

**Point d'observation :** Copilot peut proposer un contenu ou un design sans pouvoir appliquer automatiquement chaque changement. Faire constater la différence aux participants.

**Manipulations :** sélectionner une diapositive trop dense, demander une reformulation, améliorer sa disposition, puis ajouter des notes orales. Si Copilot propose un contenu à appliquer, le relire avant validation.

**Prompt 3 — Simplifier une diapositive**

```text
Améliore la diapositive des chiffres clés : conserve exactement les cinq
indicateurs, réduis le texte, mets en valeur le CA et la marge et propose
une mise en page lisible avec des blocs KPI. Ne modifie aucun chiffre.
```

**Prompt 4 — Notes du présentateur**

```text
Rédige des notes du présentateur pour la diapositive des chiffres clés :
45 secondes à l'oral, ton professionnel, explication claire de la différence
entre CA, marge et taux de marge. N'ajoute aucun résultat non fourni.
```

**Prompt 5 — Visuel pertinent**

```text
Propose un visuel sobre pour illustrer les cinq KPI sans inventer de données.
Privilégie des cartes de chiffres plutôt qu'un graphique de tendance, car
aucune série mensuelle n'est fournie. Respecte le style de la présentation.
```

**Variante manuelle :** `Insertion > Formes` ou `Insertion > Graphique` (seulement si des données de série existent), `Création > Concepteur/Designer` si disponible, `Affichage > Notes` pour les notes.

### Étape 4 — Réorganiser et synthétiser (10:00–13:00)

**Parcours guidé dans l'interface :**

1. Dans le volet Copilot, demander un résumé en trois messages clés ; comparer avec la diapositive de conclusion.
2. Demander à Copilot un diagnostic de l'ordre des diapositives, puis choisir un ordre narratif adapté à la direction.
3. Ouvrir **Affichage > Trieuse de diapositives** ou utiliser les miniatures à gauche.
4. Déplacer physiquement une diapositive par glisser-déposer ; vérifier que le sommaire correspond au nouvel ordre.
5. Si une diapositive est redondante, la masquer plutôt que la supprimer pendant la démonstration : clic droit sur la miniature, **Masquer la diapositive**.
6. Afficher les **Notes** pour contrôler les transitions orales après réorganisation.

**Manipulations :** demander une synthèse, vérifier la cohérence de l'ordre, déplacer les diapositives dans le volet de miniatures si Copilot ne le fait pas directement.

**Prompt 6 — Synthétiser**

```text
Résume cette présentation en trois messages clés pour la direction.
Distingue les résultats chiffrés vérifiés, les constats à confirmer
et les actions proposées. Signale les répétitions ou diapositives inutiles.
```

**Prompt 7 — Réorganiser**

```text
Vérifie l'enchaînement des diapositives et propose un ordre plus convaincant :
contexte, chiffres clés, analyse, priorités, décision. Indique les modifications
à effectuer et ne supprime aucun chiffre de référence.
```

**Variante manuelle :** réordonner les diapositives par glisser-déposer ; supprimer les répétitions ; raccourcir les titres.

### Étape 5 — Contrôler et enregistrer (13:00–15:00)

**Parcours guidé dans l'interface :**

1. Demander à Copilot d'auditer les chiffres, les affirmations et les répétitions.
2. Vérifier les cinq KPI à l'écran avec le briefing Word, sans accepter une simple affirmation de Copilot comme preuve.
3. Lancer **Révision > Vérifier l'accessibilité**, si disponible, et corriger au moins un avertissement pertinent.
4. Ouvrir **Diaporama > À partir du début** et vérifier rapidement la lisibilité d'une diapositive et la présence des notes.
5. Enregistrer sous `Retail360_Bilan_Commercial_2025.pptx` ; indiquer où se trouvent **Fichier > Exporter** et **Partager**.

**Prompt 8 — Audit final**

```text
Contrôle cette présentation avant diffusion : vérifie les cinq KPI du
briefing, repère les chiffres non sourcés, les formulations trop affirmatives,
les diapositives surchargées et les éventuelles incohérences. Fournis une
liste courte de corrections prioritaires, sans modifier le contenu.
```

**Contrôles manuels :**

- 600 commandes au total et 505 livrées : ne pas les inverser.
- CA = **437 100,35 €** ; marge = **126 093,35 €** ; taux global = **28,85 %**.
- Aucune tendance ou classement inventé.
- Titres, unités, lisibilité et ordre cohérents.
- Notes présentes sur au moins une diapositive.
- Enregistrer sous `Retail360_Bilan_Commercial_2025.pptx`.

## 5 bis. Banque de prompts complémentaires (hors temps principal)

Ces manipulations peuvent être proposées en démonstration ou en atelier approfondi. Elles ne sont pas toutes garanties comme actions directes de Copilot ; demander une procédure manuelle lorsque nécessaire.

### A. Créer depuis Word puis comparer

```text
Crée une présentation à partir du document Word de briefing. Compare le plan
obtenu avec celui d'une présentation créée uniquement depuis un prompt.
Signale les informations du document qui n'ont pas été reprises.
```

### B. Ajouter une diapositive de décision

```text
Ajoute une diapositive « Décisions attendues » avec trois décisions possibles :
valider les indicateurs, approfondir les segments commerciaux et définir
les priorités 2026. Présente-les comme des propositions, pas des décisions prises.
```

### C. Adapter à une autre audience

```text
Réécris les titres et les messages pour une équipe commerciale plutôt que
pour le comité de direction. Garde les chiffres inchangés et adopte un ton
plus opérationnel.
```

### D. Raccourcir une présentation longue

```text
Propose une version de 3 diapositives de ce support en conservant les
indicateurs essentiels, les limites des données et les décisions attendues.
```

### E. Créer un sommaire

```text
Crée une diapositive d'agenda courte, avec quatre parties maximum, alignée
sur l'ordre réel des diapositives.
```

### F. Générer des notes orales pour l'ensemble

```text
Rédige des notes du présentateur de 30 à 45 secondes par diapositive,
avec des transitions naturelles. Ne complète pas les données absentes.
```

### G. Améliorer l'accessibilité

```text
Évalue la lisibilité et l'accessibilité de la présentation : contraste,
taille de police, titres, texte alternatif des images et surcharge visuelle.
Propose les corrections les plus importantes.
```

### H. Appliquer une charte graphique

```text
Harmonise les diapositives autour d'un style sobre : bleu foncé, turquoise,
fond clair, titres courts et alignements réguliers. Ne modifie pas les chiffres.
```

### I. Transformer une liste en schéma

```text
Transforme les trois priorités 2026 en schéma visuel simple avec trois étapes.
Ne présente pas ces priorités comme des engagements déjà validés.
```

### J. Ajouter des résultats Excel validés

```text
Je vais fournir un tableau de synthèse vérifié depuis Excel. Propose une
diapositive de comparaison par catégorie ou région en utilisant exclusivement
ces chiffres, avec le type de graphique le plus pertinent.
```

### K. Préparer des questions-réponses

```text
Propose cinq questions que la direction pourrait poser après cette
présentation. Pour chacune, indique si le briefing permet de répondre
ou si une analyse Excel complémentaire est nécessaire.
```

### L. Préparer un résumé pour l'envoi

```text
Rédige un résumé de cette présentation en 100 mots pour accompagner son
partage aux participants, sans ajouter de faits non présents dans les slides.
```

## 6. Ateliers complémentaires — parcours fonctionnels détaillés (30 à 60 minutes supplémentaires)

Ces ateliers permettent de découvrir davantage de fonctionnalités. Ils sont **hors des 15 minutes contractuelles** et peuvent être réalisés dans l'ordre souhaité. Chaque atelier inclut une manipulation concrète, une demande Copilot et une preuve de réussite.

### Atelier A — Deux modes de création : prompt et fichier Word (6 min)

1. Créer une présentation A à partir d'une consigne textuelle décrivant Retail360.
2. Créer une présentation B à partir du briefing Word, si l'option est disponible.
3. Comparer le plan, les KPI, les titres et les informations absentes.
4. Demander : « Compare la couverture du briefing par ces diapositives et liste les éléments manquants sans inventer de données. »
5. **Preuve :** tableau de comparaison à deux colonnes, avec au moins une différence expliquée.

### Atelier B — Ajouter et modifier des diapositives (5 min)

1. Sélectionner la diapositive « Priorités 2026 ».
2. Demander à Copilot une nouvelle diapositive « Décisions attendues » avec trois décisions à valider.
3. Vérifier si Copilot l'insère ; sinon utiliser **Accueil > Nouvelle diapositive** et coller le texte proposé.
4. Sélectionner un titre et demander une version orientée résultat ; comparer avant/après.
5. **Preuve :** nouvelle diapositive, titre clair et formulation prudente.

### Atelier C — Texte sélectionné, reformulation et adaptation au public (5 min)

1. Dupliquer une diapositive avant modification (`Ctrl+D` sur Windows lorsque la miniature est sélectionnée).
2. Sélectionner un paragraphe dense et demander à Copilot de le transformer en trois puces courtes.
3. Demander une seconde version pour des commerciaux terrain, puis une version pour le comité de direction.
4. Comparer vocabulaire, longueur et niveau de détail ; conserver la version adaptée au public.
5. **Preuve :** deux versions du même message sans changement de chiffres.

### Atelier D — Design, thèmes, modèles et masque (6 min)

1. Appliquer un thème via **Création > Thèmes**.
2. Ouvrir **Création > Variantes** ou les suggestions de conception si disponibles.
3. Utiliser **Accueil > Disposition** pour uniformiser deux diapositives.
4. Ouvrir **Affichage > Masque des diapositives** pour expliquer comment centraliser styles et espaces réservés ; ne pas modifier le masque si le temps manque.
5. Demander à Copilot : « Propose des améliorations de lisibilité et de hiérarchie visuelle, sans changer les chiffres. »
6. **Preuve :** deux diapositives cohérentes en typographie et couleurs.

### Atelier E — Images, icônes, schémas et SmartArt (6 min)

1. Demander à Copilot une suggestion de visuel pour les trois priorités 2026.
2. Tester l'option de génération ou d'ajout d'image si elle est présente ; vérifier le rendu avant utilisation.
3. Alternative : **Insertion > Icônes**, **Formes** ou **SmartArt** pour représenter les trois priorités.
4. Ajouter un texte alternatif pertinent et éviter tout graphique chiffré sans données de série vérifiées.
5. **Preuve :** une diapositive plus visuelle, sans chiffres inventés.

### Atelier F — Notes, présentation orale et répétition (6 min)

1. Demander à Copilot des notes de 30 secondes par diapositive avec transitions.
2. Ouvrir le volet **Notes** et insérer ou contrôler le texte.
3. Lancer **Diaporama > Mode Présentateur** lorsque possible.
4. Tester **Répéter avec le coach** si cette fonctionnalité native est disponible ; observer les conseils sur le rythme et le langage.
5. **Preuve :** notes utilisables et durée orale cohérente.

### Atelier G — Résumer, réorganiser et condenser (5 min)

1. Demander à Copilot une synthèse en trois messages clés.
2. Demander une proposition de version condensée en trois diapositives.
3. Ouvrir **Affichage > Trieuse de diapositives** et déplacer les miniatures.
4. Masquer une diapositive redondante et vérifier la cohérence du sommaire.
5. **Preuve :** narration plus fluide, sans perte d'un KPI essentiel.

### Atelier H — Accessibilité, langue et export (5 min)

1. Lancer le vérificateur d'accessibilité et examiner ses recommandations.
2. Contrôler taille des polices, contraste, ordre de lecture et texte alternatif.
3. Demander à Copilot une reformulation en anglais d'une diapositive, **sans modifier les chiffres ni les unités** ; appliquer manuellement si nécessaire.
4. Exporter une copie PDF via **Fichier > Exporter** et conserver le PPTX éditable.
5. **Preuve :** support lisible et export conforme.

### Atelier I — Intégrer un graphique Excel vérifié (6 min)

1. Dans le classeur Excel du TP précédent, préparer un graphique par catégorie fondé uniquement sur les ventes livrées.
2. Copier le graphique et le coller dans PowerPoint, en choisissant l'option de liaison ou d'incorporation adaptée au contexte.
3. Demander à Copilot un titre orienté message et une explication courte **à partir des données réellement affichées**.
4. Vérifier les étiquettes, les unités, la source et l'absence de causalité non démontrée.
5. **Preuve :** graphique fidèle aux données et titre interprétable.

### Atelier J — Audit critique de la présentation (5 min)

1. Demander à Copilot de relever les affirmations sans preuve, les chiffres manquants et les répétitions.
2. Comparer la réponse aux cinq KPI de référence et aux diapositives réellement présentes.
3. Corriger manuellement au moins une erreur, ambiguïté ou formulation trop affirmative.
4. Documenter en une phrase la correction et sa justification.
5. **Preuve :** contrôle vérifiable et correction tracée.

### Variantes de prompts très courts pour explorer les fonctionnalités

| Besoin | Prompt à tester |
|---|---|
| Ajouter une diapositive | « Ajoute une diapositive Décisions attendues avec trois propositions à valider. » |
| Raccourcir un texte | « Réduis le texte sélectionné à trois puces de dix mots maximum. » |
| Adapter le ton | « Reformule cette diapositive pour un comité de direction. » |
| Améliorer le titre | « Propose un titre qui exprime le message principal de cette diapositive. » |
| Ajouter des notes | « Prépare 30 secondes de notes orales pour cette diapositive. » |
| Proposer un visuel | « Suggère une représentation visuelle simple des trois priorités 2026. » |
| Résumer le support | « Résume la présentation en trois messages clés, sans ajouter de faits. » |
| Détecter les répétitions | « Repère les diapositives redondantes et propose un nouvel ordre. » |
| Préparer les questions | « Propose cinq questions possibles de la direction et signale celles sans réponse. » |
| Vérifier les affirmations | « Repère les chiffres et conclusions non justifiés par le briefing. » |

---

## 7. Critères de réussite et grille d'évaluation

L'évaluation porte sur la qualité du livrable **et** sur la capacité à vérifier les réponses de Copilot. Une diapositive esthétique ne constitue pas une preuve de justesse.

| Critère | Points | Preuve attendue |
|---|---:|---|
| Prompt adapté au public et à la source | 2 | Objectif, audience, longueur et source explicites |
| Fidélité des KPI et absence de chiffres inventés | 3 | Comparaison avec le briefing |
| Structure et logique de présentation | 2 | Plan, progression et conclusion clairs |
| Lisibilité, mise en page et notes | 2 | Support projetable, notes utiles |
| Vérification critique | 1 | Au moins une correction ou limite documentée |
| **Total** | **10** | **Seuil conseillé : 7/10** |

**Critère bloquant pédagogique :** un chiffre commercial inventé ou une erreur non corrigée sur un KPI majeur doit être signalé, même si la présentation est visuellement réussie.

## 8. Dépannage rapide

| Symptôme | Vérification / solution |
|---|---|
| Copilot absent | Vérifier licence, application, compte connecté et politique administrateur |
| Word non proposé comme source | Vérifier accès au fichier, emplacement cloud et fonction disponible ; utiliser le texte du briefing dans le prompt |
| Présentation trop longue | Demander 5 à 6 diapositives maximum ; supprimer manuellement les doublons |
| Chiffres incorrects | Corriger depuis le tableau de référence ; ne pas demander à Copilot de les estimer |
| Notes non créées | Demander le texte des notes puis le coller dans le volet Notes |
| Mise en page non appliquée | Utiliser le thème, les dispositions et les outils de conception de PowerPoint |
| Graphique non pertinent | Ne créer de graphique de série que si les données correspondantes existent |
| Images non cohérentes | Préférer icônes simples ou visuels de marque, vérifier les droits et la pertinence |
| Action non disponible dans Copilot | Demander une procédure détaillée puis effectuer l'action dans le ruban PowerPoint |

## 9. Conseils au formateur

- **Faire une démonstration courte et visible** : un prompt de création, un prompt d'amélioration, un prompt de contrôle.
- **Ne pas surcharger les 15 minutes** : choisir 5 à 6 diapositives et ne travailler en profondeur qu'une diapositive.
- **Garder le briefing ouvert** pour vérifier les chiffres immédiatement.
- **Éviter l'effet “magie”** : montrer une erreur ou une limite de Copilot et sa correction.
- **Relier Excel et PowerPoint** : expliquer que la présentation communique des analyses déjà vérifiées, elle ne remplace pas le calcul dans Excel.
- **Prévoir un plan B** : création de diapositives et notes par copier-coller, puis amélioration avec les fonctions natives de PowerPoint.

## 10. Livrables attendus

1. `Retail360_Bilan_Commercial_2025.pptx` : présentation finale de 5 à 6 diapositives.
2. Au moins une diapositive améliorée après génération initiale.
3. Des notes du présentateur sur une diapositive au minimum.
4. Une vérification documentée des cinq KPI et des affirmations commerciales.

---

*Support pédagogique fictif — MS-4018 / Microsoft 365 Copilot dans PowerPoint. Les fonctionnalités disponibles varient selon les versions et configurations Microsoft 365.*
