# FO Énergie GRDF — Ma liste CSE 2027

Outil web des militants Force Ouvrière pour composer une liste de candidats au **Comité Social et Économique 2027** qui ne puisse pas être annulée, savoir combien de voix aller chercher, et déposer sereinement.

**En ligne :** https://FO-GRDF.github.io/fo-cse-listes-2027/

---

## Le parcours en quatre étapes

1. **Les chiffres** — trois nombres par collège : femmes inscrites, hommes inscrits, sièges. Ils sont dans le protocole d'accord préélectoral (L. 2314-13). Saisie directe, ou import d'un fichier Excel anonymisé (sexe, collège, établissement) dont l'outil ne conserve que les totaux.
2. **La liste** — pour chaque collège et chaque liste (titulaires, suppléants), on choisit le nombre de candidats présentés ; l'outil dessine les cases dans le bon ordre (proportion du collège + alternance, L. 2314-30) et vérifie en direct ce qui est réellement saisi : proportion sur les candidats présentés, alternance jusqu'à épuisement, première position, règle des deux sièges, doublons.
3. **Les voix** — quotient électoral et seuils garantis par taux de participation (R. 2314-19) ; avec les scores 2023 (saisis ou lus dans les PV CERFA), projection à la plus forte moyenne (R. 2314-20) et voix FO nécessaires siège par siège.
4. **Le dépôt** — date limite du PAP avec décompte, bilan de conformité de toutes les listes, checklist candidat par candidat (L. 2314-19), PDF de dépôt, envoi au syndicat.

Annexes : prestataires électeurs (L. 2314-23), textes et décisions vérifiés, sauvegarde et aide.

## Ce qui protège le militant

- Les **voyants sont calculés**, pas décoratifs : une liste incomplète, un candidat seul pour deux sièges, une liste « paritaire » dans un collège déséquilibré sont signalés comme **annulables**, avec la règle et la décision qui l'ont dit.
- Le travail est **sauvegardé automatiquement** dans le navigateur et peut être exporté / repris en `.json`.
- Le PDF porte le vrai logo FO, l'état de conformité de chaque liste et le cadre légal.

## Confidentialité

Aucune donnée ne sort du navigateur : pas de serveur, pas d'envoi. Le fichier Excel importé est réduit à des totaux par collège avant sauvegarde. Les noms des candidats restent sur l'appareil de l'utilisateur. Utilisable hors ligne après le premier chargement.

## Cadre légal (vérifié Légifrance le 3 septembre 2026)

| Texte | Objet |
|---|---|
| [L. 2314-30](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000035651024) | Proportion F/H du collège, alternance, arrondi, candidat du sexe non représenté jamais en tête |
| [L. 2314-32](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000035615701) | Annulation des élus en surnombre / mal positionnés |
| [L. 2314-19](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000046774664) | Éligibilité |
| [L. 2314-13](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000036262464) | Le PAP mentionne la proportion F/H de chaque collège |
| [L. 2314-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000037389707) | Autant de suppléants que de titulaires |
| [R. 2314-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000036481896) | Nombre de titulaires selon l'effectif |
| [L. 2314-29](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000035651029) | Scrutin, quorum, ratures |
| [R. 2314-19](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000018485529) · [R. 2314-20](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000018485531) | Quotient, plus forte moyenne |
| [L. 2314-23](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006901895) | Salariés mis à disposition |

Décisions : [Cass. soc. 9 mai 2018, n° 17-14.088](https://www.legifrance.gouv.fr/juri/id/JURITEXT000036930102) (deux sièges, candidat unique annulé) · [Cass. soc. 17 avril 2019, n° 17-26.724](https://www.legifrance.gouv.fr/juri/id/JURITEXT000038488520) (liste « paritaire » annulée ; liste incomplète admise à proportion des candidats présentés) · [Cass. soc. 25 novembre 2020, n° 19-60.222](https://www.legifrance.gouv.fr/juri/id/JURITEXT000042619658) (candidatures libres du second tour non soumises).

## Technique

Un seul fichier `index.html` (CSS et JS inclus, logo embarqué). Bibliothèques CDN : SheetJS (Excel), jsPDF + AutoTable (PDF), pdf.js (lecture des CERFA). Hébergement GitHub Pages, fichier `.nojekyll`. Statistiques anonymes GoatCounter.

## Contact

syndicat-fo_grdf-delegations-nationales@grdf.fr · Instagram [@FO_GRDF](https://www.instagram.com/FO_GRDF)
