## Approche
- Extraction des points de repère de la main avec MediaPipe (détection réussie sur 7 509 des 15 000 images), puis classification par un MLP (93,7 % sur les images où une main est détectée)
- CNN entraîné sur les images en niveaux de gris 28×28 avec augmentation de données (88,3 %)
- Classifieur hybride : somme des probabilités des deux modèles quand MediaPipe détecte une main, CNN seul sinon (93,6 % sur 3 000 images de test)

## Lancer le projet
1. Ouvrir le notebook dans Google Colab (bouton ci-dessus).
2. Créer un token Kaggle (Kaggle → Settings → API → Create New Token).
3. Dans Colab, ajouter les secrets `KAGGLE_USERNAME` et `KAGGLE_KEY` (icône clé à gauche) avec les valeurs du token.
4. Exécuter toutes les cellules.

## Limites
- MediaPipe ne détecte pas la main sur environ la moitié des images : le CNN prend alors le relais.
- Le jeu de données est peu varié (fonds et mains similaires) : les performances sur des photos réelles seront plus faibles.
