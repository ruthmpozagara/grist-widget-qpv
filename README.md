# Vérificateur QPV

Ce widget permet de vérifier si des coordonnées géographiques (latitude, longitude) se situent dans un Quartier Prioritaire de la Ville (QPV) en France. Il exploite les données issues du fichier "Périmètre des QPV au format geojson (EPSG:4326)" (Mis à jour le 27 juin 2024) hébergées sur data.gouv et remplit automatiquement les colonnes d'un tableau Grist avec les résultats d'analyse. 

## Utilisation via le custom widget builder 
1. **Copier coller le contenu du fichier widget-qpv.html.**
2. **Ajoutez le widget à votre document Grist** via le custom widget builder.
3. **Configurez les colonnes** dans le panneau de création :
   * `Latitude` : Colonne contenant les latitudes.
   * `Longitude` : Colonne contenant les longitudes.
   * `Est en QPV`: Colonne booléenne (true/false).
   * `Nom du QPV`: Colonne de texte pour le nom du quartier
   * `Code du QPV` : Colonne de texte pour le code du quartier.
4. **Cliquez sur "Analyser les coordonnées"** une fois les colonnes configurées pour lancer l'analyse.

## Dépendances
* Turf.js
* Grist Plugin API
