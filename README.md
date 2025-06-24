# Vérificateur QPV

Ce widget permet de vérifier si des coordonnées géographiques (latitude, longitude) se situent dans un Quartier Prioritaire de la Ville (QPV) en France. Il exploite les données issues du fichier "Périmètre des QPV au format geojson (EPSG:4326)" hébergées sur data.gouv et remplit automatiquement les colonnes d'un tableau Grist avec les résultats d'analyse. 

## Fonctionnalités 
* Vérification automatique de la présence d'un point dans un QPV à partir de coordonnées.
* Remplissage des colonnes : présence en QPV (booléen), nom et code du QPV.
* Chargement dynamique des données QPV depuis data.gouv.fr.
* Utilisation de Turf.js pour la géolocalisation de l'API Grist Plugin.

## Installation 
1. **Téléchargez ou clonez ce dépôt.**
2. **Ajoutez le widget à votre document Grist** via le custom widget builder.
3. **Configurez les colonnes** dans le panneau de création :
   * `Latitude` : Colonne contenant les latitudes.
   * `Longitude` : Colonne contenant les longitudes.
   * `Est en QPV`: Colonne booléenne (true/false).
   * `Nom du QPV`: Colonne de texte pour le nom du quartier
   * `Code du QPV` : Colonne de texte pour le code du quartier.
  
## Utilisation 
* Cliquez sur **"Analyser les coordonnées"** une fois les colonnes configurées pour lancer l'analyse.
* Le widget télécharge les données QPV, puis vérifie chaque ligne du tableau.
* Les résultats sont automatiquement inscrits dans les colonnes configurées.
* Utilisez le bouton **"Afficher/Masquer débogage"** pour consulter le journal d'exécution en cas de problème.

## Dépendances
* Turf.js
* Grist Plugin API
