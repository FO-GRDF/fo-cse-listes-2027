# FO GRDF — Constructeur de liste électorale CSE 2027

Outil web autonome destiné aux militants Force Ouvrière pour construire les listes de candidats aux élections du **Comité Social et Économique 2027**, en stricte conformité avec le Code du travail.

**Outil en ligne :** https://FO-GRDF.github.io/fo-cse-listes-2027/

---

## Ce que l'outil fait

À partir d'un fichier Excel **anonymisé** des salariés de l'établissement (uniquement les colonnes sexe, collège, établissement), l'outil :

- calcule automatiquement le **nombre de sièges titulaires et suppléants** selon l'effectif (art. R. 2314-1),
- détermine pour chaque collège la **proportion légale F/H** sur la liste (art. L. 2314-30),
- génère des **slots de candidats** pré-cadrés avec **alternance F/H imposée** (jusqu'à épuisement du sexe minoritaire),
- affiche en temps réel des **indicateurs de conformité** (vert / orange / rouge),
- calcule le **nombre de voix nécessaires** pour faire élire 1, 2, 3… militants FO selon différents taux de participation (art. R. 2314-19),
- exporte la liste finale en **Excel et PDF** prêts pour le Protocole d'Accord Préélectoral (PAP),
- fournit un **guide pédagogique + checklist** pour s'assurer du droit de vote des prestataires (art. L. 2314-23).

---

## RGPD — sécurité absolue

**Aucune donnée ne sort de votre navigateur.** Le fichier des salariés est lu et traité 100 % localement, en JavaScript pur. L'outil n'envoie rien sur Internet, ne stocke rien, n'a pas de back-end.

Vous pouvez l'utiliser hors ligne après le premier chargement.

---

## Cadre légal validé (sources Légifrance)

| Article | Objet |
|---|---|
| [L. 2314-11](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006901882) | Composition des collèges (3ᵉ collège dès 25 cadres) |
| [R. 2314-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000018485479) | Tableau nombre de titulaires par effectif |
| [L. 2314-30](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006901904) | Représentation équilibrée F/H + alternance + arrondi |
| [L. 2314-32](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000035615701) | Sanctions du juge en cas de non-respect |
| [L. 2314-29](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006901903) | Scrutin proportionnel 2 tours, quorum 50 %, ratures 10 % |
| [R. 2314-19](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000018485529) | Quotient électoral = SVE ÷ sièges |
| [R. 2314-20](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000018485531) | Plus forte moyenne |
| [L. 2314-23](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006901895) | Éligibilité des prestataires (12 mois, droit de choix) |
| [L. 1111-2](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006900783) | Calcul des effectifs |

---

## Structure du fichier d'entrée

L'outil reconnaît automatiquement les colonnes contenant les mots-clés `SEXE`, `COLLEGE`/`COLLÈGE`, et `UM`/`UNITE`/`ETABLISSEMENT`. Variantes de valeurs acceptées :

- **Sexe** : `Masculin/Féminin`, `M/F`, `H/F`, `Homme/Femme`
- **Collège** : `Exécution`, `Maîtrise`, `Cadre` (ou `1`, `2`, `3` / `I`, `II`, `III` / `1er`, `2ème`, `3ème`)

Les lignes contenant `#N/A` ou valeurs manquantes sont automatiquement exclues et signalées.

Voir l'exemple de structure dans l'onglet "Import fichier" de l'outil.

---

## Architecture technique

- **Single-file HTML** autonome (`index.html`)
- **CSS inline** avec palette FO GRDF + mode lecture universelle (accessibilité daltoniens/dys)
- **JS inline** + librairies CDN :
  - [SheetJS](https://sheetjs.com/) pour lecture/écriture Excel
  - [jsPDF](https://github.com/parallax/jsPDF) + [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) pour export PDF
- **Hébergement** : GitHub Pages (gratuit, https, hors ligne après cache)
- **Analytics** : GoatCounter (anonyme, RGPD-friendly)

---

## Contact

📧 **syndicat-fo_grdf-delegations-nationales@grdf.fr**
📱 Instagram : [@FO_GRDF](https://www.instagram.com/FO_GRDF)

---

*Outil développé pour les militants FO Énergie GRDF · CSE 2027 · Données salariées jamais transmises.*
