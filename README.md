# Analyse des appels 3CX

Tableau de bord d'analyse des exports d'appels 3CX du standard SOS92.

## Utilisation

1. Ouvrez la page (GitHub Pages) ou le fichier `index.html` dans un navigateur.
2. Cliquez sur **Importer des CSV** (ou glissez-déposez les exports 3CX sur la page). Plusieurs jours peuvent être ajoutés à la suite ; les doublons sont ignorés.
3. Filtrez par période, plage horaire, issue, agents ou files, ou cliquez sur les barres des graphiques.

Les données restent dans le navigateur de chaque utilisateur : rien n'est envoyé sur Internet ni dans ce dépôt.

## Ce que calcule l'outil

- Chaque appel est reconstitué à partir de toutes ses lignes 3CX (même Call ID) : SVI, file d'attente, agent, parking, transfert.
- **Taux de décroché total** = répondus ÷ (répondus + abandons en file + abandons au SVI), hors appels courts (seuil réglable, 10 s par défaut).
- **Taux en file** = répondus ÷ appelants arrivés en file. **Passage du SVI** = appelants arrivés en file ÷ tous les appelants. Total = SVI × en file.
- Les heures sont lues telles qu'écrites par 3CX, sans conversion de fuseau.
- Exclus : fax (888), codes de service (*77*…), ligne « Totals » de l'export.
