# Résumé : Application et Résultats

## Introduction
Dans cette section, nous présentons les étapes de mise en œuvre du modèle SciBERT pour analyser la corrélation entre les citations et les références des articles scientifiques. L'extraction des textes de référence est réalisée à l'aide de Grobid, puis ces textes sont traités afin de calculer des scores de similarité. Ce travail a été réalisé en utilisant le dataset **FullTextPeerRead**, qui contient des articles scientifiques pour analyser la corrélation entre les citations et les références.

## 1. Préparation des données
### Flux de données
![Récupération des ids](/images/.png)
- Identification des articles sources et cibles via `source_id` et `target_id`.

### Téléchargement des Fichiers PDF
![Téléchargement des articles scientifiques](/images/2.1.png)
- Les articles sont téléchargés automatiquement depuis des bases de données scientifiques.

### Conversion en XML avec Grobid
![Utilisation de Grobid software](/images/3.png)
- Conversion des PDFs en XML structuré pour extraire les métadonnées et références.

### Extraction des Citations et Références
![Code extraction de texte](/images/5.png)
- Extraction des sections textuelles pertinentes des fichiers XML.

### Résultat de l'extraction
![Résultat de l'extraction de texte](/images/6.png)

### Association de Texte avec les Citations
![Code d'association de texte avec les citations](/images/7.png)
- Liaison des textes extraits avec les métadonnées des articles.

## 2. Application du modèle SciBERT
### Chargement du modèle
![Chargement du modèle](/images/9.png)
- Utilisation de SciBERT pour analyser la similarité sémantique.

### Calcul de la similarité cosinus
![Cosinus Similarité](/images/10.png)
- Mesure de l'angle entre les vecteurs des citations et des références.

### Résultat des calculs
![Résultat de calcul](/images/13.png)
- Analyse statistique des similarités obtenues.

## 3. Visualisation des résultats
### Statistiques descriptives
![Statistiques descriptives](/images/14.png)
- Analyse des distributions des scores de similarité.

### Graphique de similarité
![Graph de similarité](figure_33.png)
- Répartition des valeurs de similarité entre les citations et les références.

### Graphique de régression
![Graph de régression](figure_34.png)
- Mise en évidence d'une tendance positive entre les citations et les références.

## Conclusion
L'analyse a montré une forte corrélation entre les citations et leurs références, avec des scores de similarité élevés. L'utilisation de SciBERT s'est révélée efficace pour quantifier ces relations, ouvrant la voie à des améliorations dans les outils d'analyse des citations académiques.
