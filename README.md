# Computer Vision

Le Computer Vision pré-existait avant le Deep Learning. Des techniques classiques de CV :

- filtrage

- détection de traits (bords, coins, objets)

- segmentation

## Pour commencer

Installer Anaconda sur sa machine et travailler en local dans un répertoire que l'on mettra sur github à terme.  
Créer un environnement conda à partir du fichier environment_cv.yml situé dans le dossier environnement.  
Les développements se font dans des notebooks Jupyter. 

## Les datasets

Nous utiliserons 3 datasets :

- Sign Language Digits: Il s'agit de photos de mains formant les 10 chiffres en langage des signes. Le dataset est disponible [ici](https://www.kaggle.com/hamishdickson/preprocessing-images-with-dimensionality-reduction/data).

- Fashion MNIST: Une base d'images de vêtements fournie par Zalando, qui se trouve [ici](https://www.kaggle.com/zalando-research/fashionmnist).


- Galaxy Zoo: Une base d'images extraites du projet Galaxy Zoo.
Les données sont volumineuses (téléchargement : galaxy zoo data).

## Test avec OpenCV

### Introduction à OpenCV (cv2): 

- Traitement d'une image et transformations: OpenCV.ipynb

### Exercice avec OpenCV:

OpenCV_exo.ipynb

- Pour les images chargées en couleurs BGR, les convertir en HSV et en YUV
- Choisir 5 images contenant des flammes (exemples : bougie, feu de cheminée, incendie, etc.) et 5 images sans flammes, les sauver dans un sous-répertoire images
- En utilisant la bibliothèque cv2, appliquer une fonction de changement de taille d'image d'opencv à toutes les images précédentes et sauvegarder les images avec leur nouvelle taille dans le répertoire images avec un suffixe "_resized" et dans un encodage de votre choix (exemples : jpg, png, etc.).
- Réfléchir à comment utiliser les espaces de couleur pour segmenter les images contenant des flammes pour isoler les zones contenant les flammes
- Fabriquer des images binaires à partir de la segmentation précédente

## Atelier sur le thème de la réduction de la dimensionnalité

Utiliser scikit-learn pour mettre en pratique sur le datasets 1  la méthode suivante :

PCA: PCA.ipynb

## Classification d'images sans CNN

Appliquer des SVM au dataset 2 pour la classification. 
Evaluer la performance de l'algorithme choisi.

SVM: SVM.ipynb

## Data Augmentation

Choisir 9 images quelconques de Hand Digits
Générer des variantes avec les fonctions de Data Augmentation de Keras:
DataAugmentation.ipynb  

Voir ImageDataGenerator()
- Appliquer une translation aléatoire
- Appliquer une rotation aléatoire
- Appliquer feature standardization
- Appliquer le ZCA whitening (des explications [ici](https://cbrnr.github.io/2018/12/17/whitening-pca-zca/)).

## Haar cascade with OpenCV

Lecture sur les cascades de Haar : [ici](https://pymotion.com/detection-objet-cascade-haar/).

Vidéo youtube exlicative pour [Haar cascade with OpenCV](https://www.youtube.com/watch?v=88HdqNDQsEk).

- Reconnaissance de la face d'un chat à partir de photo: Haar_cascade_catface.ipynb
- Reconnaissance de la face d'un homme à partir d'une vidéo: Haar_cascade_face_eye_recognition.ipynb et Haar_cascade_face_eye_smile_profile_recognition.ipynb

## Challenge Galaxy Zoo

### Préparation des données
Choix de la classe1, traitement des données, algorithmes de compression des images: 
- Galaxy_zoo_Class1_separation.ipynb
- Galaxy_zoo_Class1_treatment.ipynb

### Transfer learning
Choix d'un modèle sur étagère:
- CNN_Pretrained_CNN.ipynb sur sign language.

### Application sur un sous-ensemble de Galaxy Zoo: 

Application à la classe 1 de Galaxy Zoo: Galaxy_zoo_modelCNN.ipynb
