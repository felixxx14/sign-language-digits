# Reconnaissance des chiffres en langue des signes

Classifieur hybride de vision par ordinateur qui reconnaît les 10 chiffres (0 à 9) de la langue des signes à partir d'images de mains.


## Résultats
- **93,6 % de précision** sur 3 000 images de test (modèle hybride)
- 88,3 % de précision avec le CNN seul

## Approche
- Points de repère de la main extraits avec MediaPipe, puis classés par un réseau de neurones
- CNN entraîné directement sur les images
- Les deux modèles sont combinés en un classifieur hybride : [une phrase sur la façon dont vous les combinez]

## Jeu de données
15 000 images issues de Kaggle : [nom du dataset et lien].
Les images ne sont pas dans ce dépôt : le notebook les télécharge avec l'API Kaggle.

## Lancer le projet
1. Ouvrir le notebook dans Google Colab (bouton ci-dessus).
2. Créer un token API Kaggle (Kaggle → Settings → API → Create New Token).
3. Importer le fichier `kaggle.json` téléchargé quand le notebook le demande.
4. Exécuter toutes les cellules.

## Technologies
Python, TensorFlow/Keras, MediaPipe, scikit-learn, Google Colab
