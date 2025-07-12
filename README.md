# expressionLabiale

### Projet de Lecture Labiale à partir de Vidéos (Lip Reading)
Ce projet vise à reconnaître des mots prononcés silencieusement à partir de séquences vidéo des mouvements labiaux (lèvres), à l’aide d’un modèle d’apprentissage profond. Chaque vidéo est transformée en une séquence d’images (frames), puis traitée pour entraîner un modèle CNN+LSTM capable de prédire les mots prononcés.

### Structure du dataset
    Les vidéos sont converties en dossiers d’images selon l’organisation suivante :
    dataset_final/
    ├── mot1/
    │   ├── mot11/ → contient les frames de la vidéo mot1 par une personne
    │   ├── mot12/
    │   └── ...
    ├── mot2/
    │   ├── mot21/
    │   ├── ...
    └── ...
Chaque sous-dossier (mot11, mot12, etc.) 
contient les frames extraites d’une vidéo de la prononciation d’un mot spécifique.
### Entraînement
    Les séquences d’images sont redimensionnées et normalisées.
    
    Un modèle CNN + LSTM est utilisé :
    
    CNN pour extraire des caractéristiques spatiales de chaque frame
    
    LSTM pour capturer la dynamique temporelle des séquences
    
    Les performances sont évaluées via la précision, la matrice de confusion, et la courbe d’apprentissage.

### Utilisation
    Entraînement du modèle : train_model(dataset_path)
    
    Test en temps réel avec la webcam ou vidéo existante
    
    Modèle exporté au format .h5 pour une réutilisation directe
