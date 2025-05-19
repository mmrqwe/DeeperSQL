# Tutoriel Détaillé du Logiciel DeeperSQL
## Changement de langue
[English](README.md)

## Contenu du Tutoriel
* 1. Introduction au Logiciel
* 2. Installation & Lancement
* 3. Fonctionnalités Principales
* 4. Étapes d'Opération
* 5. FAQ
* 6. Contact & Support

## 1. Introduction au Logiciel
DeeperSQL est un outil multifonctionnel qui intègre l'interaction intelligente avec Excel, la construction de graphes de connaissances, les questions-réponses par IA, la visualisation de données, et plus encore. Il convient à l'édition et à l'analyse de données, à la gestion des connaissances, aux questions-réponses intelligentes, et à divers autres scénarios.
* Après avoir importé des fichiers Excel, vous pouvez les traiter et les exporter en utilisant le langage naturel.
* Composants graphiques intégrés pour l'analyse et la visualisation des données
* Les graphes de connaissances peuvent être construits via de grands modèles de langage pour des questions-réponses intelligentes
* Support multiplateforme (Windows/macOS)

## 2. Installation & Lancement
### 2.1 Configuration Requise
* Système d'exploitation : Windows 10/11 ou macOS
* Dépendances : .NET 8.0 ou supérieur
### 2.2 Étapes d'Installation
1. Téléchargez le dernier package d'installation.
2. Assurez-vous du support des composants .NET, avec le support des grands modèles en ligne/hors ligne et des modèles embarqués.
3. Exécutez le programme principal `DeeperSQL`.
### 2.3 Lancement du Logiciel
1. Double-cliquez sur le fichier exécutable.
2. Pour le premier lancement, configurez les paramètres du grand modèle de langage pour assurer un fonctionnement correct.

## 3. Fonctionnalités Principales
### 3.1 Interaction Intelligente avec Excel
Après avoir importé des fichiers Excel, vous pouvez les sauvegarder dans une base de données et les traiter, analyser, et exporter en utilisant le langage naturel.
### 3.2 Graphe de Connaissances
Supporte la génération automatique, la visualisation et l'interrogation des nœuds, relations et communautés du graphe de connaissances. Le logiciel génère automatiquement des graphes de connaissances en utilisant de grands modèles de langage.
### 3.3 Questions-Réponses par IA
Le module de questions-réponses par IA supporte l'intégration avec divers grands modèles de langage. Les utilisateurs peuvent poser des questions en langage naturel et sélectionner des graphes de connaissances générés pour les questions-réponses.
### 3.4 Analyse de Données
Les fichiers Excel importés peuvent être analysés et visualisés après avoir été stockés dans la base de données.
### 3.5 Service API
Fournit des services API pour l'interaction SQL intelligente.

## 4. Étapes d'Opération
### 4.1 Paramètres
1. Cliquez sur Paramètres dans l'interface principale, puis sélectionnez "Setting".
2. Après l'apparition de l'interface des paramètres, cliquez sur l'onglet LLM, sélectionnez un fournisseur de modèle courant, entrez l'adresse de l'API, saisissez la clé API si nécessaire, et sélectionnez le modèle correspondant.
3. Entrez des limites appropriées pour les appels API par minute et les limites de jetons. Les API en ligne ont généralement des limites plus basses (10-30), et les limites de jetons devraient être d'au moins 4096 mais généralement inférieures à 10240 (ajustez selon les conditions réelles).
4. Ensuite, entrez l'adresse API et la clé API du modèle embarqué, et sélectionnez le modèle correspondant. Si localhost ne fonctionne pas pour les modèles locaux, essayez d'utiliser 127.0.0.1.
5. En cas de problèmes lors du chargement du modèle, une popup apparaîtra. Assurez-vous que le modèle se charge correctement.
6. Si vous cochez "Utiliser des données d'exemple pour les requêtes SQL", la première ligne de données de la table de la base de données sera utilisée comme données d'exemple. Si la confidentialité est une préoccupation, utilisez un LLM local ou décochez cette option.
7. Si vous cochez "Utiliser l'indexation du texte original", cela augmentera l'utilisation des jetons mais améliorera la précision de la recherche.
### 4.2 Création de Graphes de Connaissances
1. Cliquez sur Base de Connaissances dans l'interface principale, puis sélectionnez le sous-élément Base de Connaissances.
2. Dans l'interface de la base de connaissances, sélectionnez un nœud dans l'arborescence à gauche et faites un clic droit.
3. Après l'apparition de la boîte de sélection, cliquez sur Ajouter un Groupe, entrez le nom du groupe, et cliquez sur Confirmer.
4. Après l'ajout, cliquez sur le groupe dans le contrôle des propriétés et cliquez sur Ajouter dans la barre de menu supérieure, puis sélectionnez les fichiers à ajouter.
5. Attendez patiemment la fin de la génération du graphe de connaissances. Si aucune erreur ne se produit, la création est réussie.
6. Dans l'interface de la base de connaissances, sélectionnez un nœud dans l'arborescence à gauche, faites un clic droit, et après l'apparition de la boîte de sélection, cliquez sur Importer un Groupe ou Exporter un Groupe.
### 4.3 Gestion des Graphes de Connaissances
1. Cliquez sur Base de Connaissances dans l'interface principale, puis sélectionnez le sous-élément Base de Connaissances.
2. Dans l'interface de la base de connaissances, sélectionnez un nœud dans l'arborescence à gauche et faites un clic droit.
3. Après l'apparition de la boîte de sélection, cliquez sur Supprimer le Groupe, Importer le Groupe, ou Exporter le Groupe pour effectuer ces fonctions.
4. Sélectionnez le nœud par défaut, cliquez sur "Modèle" dans la barre de menu pour exporter la base de données "like", ou cliquez sur "Importer" pour l'importer. Cliquez sur Modifier ou Supprimer pour modifier ou supprimer un contenu "like" spécifique.
### 4.4 Visualisation des Graphes de Connaissances
1. Dans l'interface de gestion des graphes de connaissances, sélectionnez une base de connaissances et cliquez sur le bouton "Graphe de Connaissances".
2. Après être entré dans l'interface de visualisation des graphes de connaissances, cliquez sur les nœuds ou arêtes respectifs, puis cliquez sur le bouton Visualiser pour voir les données correspondantes.
3. Entrez le contenu de la recherche, appuyez sur Entrée, et les résultats de recherche correspondants seront affichés.
### 4.5 Ajout de Fichiers Excel
1. Sélectionnez le menu "Fichiers", cliquez sur "Ouvrir", et sélectionnez un fichier Excel.
2. Après une importation réussie, cliquez sur Base de données, entrez un nom de base de données, et cliquez sur Enregistrer. (Note : La première ligne de la feuille Excel est automatiquement reconnue comme les noms des champs de la table de la base de données)
3. Cliquez sur la base de données que vous venez de sauvegarder, puis cliquez sur Charger pour charger la base de données dans la table actuelle.
### 4.6 Édition des Tables de la Base de Données
1. Après avoir ouvert un fichier Excel ou chargé une base de données, vous pouvez sélectionner des fonctions comme "Copier, Coller, Annuler, Rétablir, Ajouter une Colonne, Ajouter une Ligne" dans le menu "Modifier".
2. Cliquez sur la table et faites un clic droit pour sélectionner les fonctions correspondantes.
3. Cliquez sur les éléments de la table (par ex., sheet1) dans la barre de menu pour créer, supprimer ou renommer les éléments de la table de la base de données.
### 4.7 Analyse Statistique
1. Après avoir chargé une base de données, cliquez sur le bouton "Statistiques" dans l'interface principale pour accéder à la page "Statistiques de la base de données".
2. Sélectionnez la base de données et la table que vous souhaitez analyser.
3. Sélectionnez les champs à analyser, cliquez sur le bouton Analyser, et visualisez les résultats de l'analyse. Cliquez sur Exporter pour exporter les résultats de l'analyse.
### 4.8 Interaction Intelligente avec Excel
1. Après avoir ajouté un fichier Excel et sauvegardé la base de données, chargez cette base de données.
2. Entrez une question en langage naturel en bas à droite de l'interface principale et cliquez sur le bouton "Générer".
3. Après le traitement par le LLM, une boîte de dialogue apparaît automatiquement. Confirmez que le SQL généré est faisable, puis cliquez sur Exécuter pour générer les résultats. (Supporte la production de plusieurs résultats, par ex., générer douze résultats par mois)
4. Cliquez sur Exporter et sélectionnez un dossier pour exporter les résultats sous forme de table Excel. Cliquez sur le bouton "J'aime" pour fournir des commentaires à la base de données locale (les données ne sont pas téléchargées), aidant le logiciel à générer des résultats plus précis.
### 4.9 Conversation IA
1. Sélectionnez le menu "Base de Connaissances", puis cliquez sur "Chat".
2. Sans cliquer sur l'arborescence de la base de connaissances à gauche, entrez une question dans la zone de saisie, cliquez sur le bouton "Commencer à chatter", et attendez que les résultats soient générés.
3. Cliquez sur l'arborescence de la base de connaissances à gauche pour charger la base de connaissances correspondante, entrez une question dans la zone de saisie, cliquez sur "Commencer à chatter", et attendez les résultats. Une fois les résultats générés, cliquez sur Références ou Historique pour afficher le contenu associé.
### 4.10 Service API
* /api/SQL/List Obtenir la liste des bases de données
* /api/SQL/Tables Obtenir la liste des tables de la base de données spécifiée Param : dbname
* /api/SQL/TableInfo Obtenir la structure de la table et le nombre de lignes Param : dbname, tablename
* /api/SQL/Get Obtenir les données de la table par page Param : dbname, tablename, start, num
* /api/SQL/Chat Questions-réponses SQL intelligentes Param : dbname, content
* /api/SQL/Do Exécuter une instruction SQL Param : dbname, content
* /api/status État du service

## 5. FAQ
### Q1 : Que dois-je faire en cas d'erreur au démarrage ?
**A1 :** Veuillez vérifier si l'environnement .NET est installé, ou consultez le fichier journal pour des informations d'erreur détaillées.
### Q2 : Que dois-je faire en cas d'erreur lors de l'importation de fichiers Excel ou de la création d'une base de données ?
**A2 :** Veuillez vous assurer que la première ligne du fichier Excel contient les noms des champs de la base de données, et que le format des données Excel est correct. Par exemple, les champs de date dans la table de la base de données doivent être au format "2025-12-30".
### Q3 : Que dois-je faire en cas d'erreur lors du chargement du modèle ?
**A3 :** Tout d'abord, confirmez si l'adresse du modèle est correcte. Si une clé API est requise, assurez-vous d'avoir entré la bonne clé API. Vérifiez si les préfixes http/https sont corrects, si le réseau est normal, etc. Après avoir changé l'adresse, redémarrez le logiciel pour tester.
### Q4 : Que dois-je faire en cas d'erreur avec la conversation IA ?
**A4 :**
1. Assurez-vous que l'adresse du modèle, la clé API, etc. sont corrects.
2. Assurez-vous que le réseau est normal.
3. Pour les modèles locaux, assurez-vous que le service du modèle fonctionne correctement.
4. Pour les modèles en ligne, assurez-vous que la clé API est correcte.
5. Assurez-vous que les limites de jetons, les limites d'appels API par minute, etc. sont correctes—ni trop élevées ni trop basses.

## 6. Contact & Support
Pour des questions ou suggestions, veuillez contacter l'équipe de développement :
* Email : deepersql@hotmail.com
