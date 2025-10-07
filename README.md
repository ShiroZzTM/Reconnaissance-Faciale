# 🎯 OpenCV Face Recognition

Système complet de reconnaissance faciale en Python avec détection multi-fonctionnelle utilisant OpenCV et des cascades de Haar.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📋 Table des Matières

- [À Propos](#à-propos)
- [Fonctionnalités](#fonctionnalités)
- [Architecture du Projet](#architecture-du-projet)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Structure des Fichiers](#structure-des-fichiers)
- [Technologies Utilisées](#technologies-utilisées)
- [Exemples](#exemples)
- [Contribution](#contribution)
- [Auteur](#auteur)

## 🎓 À Propos

Ce projet implémente un système complet de reconnaissance faciale utilisant les algorithmes de détection par cascades de Haar d'OpenCV. Il permet la détection en temps réel de visages, d'yeux et de sourires, ainsi que l'entraînement de modèles personnalisés pour l'identification d'individus spécifiques.

Le système est conçu avec une architecture modulaire facilitant l'extension et la maintenance du code.

## ✨ Fonctionnalités

- **Détection multi-fonctionnelle** :
  - Détection de visages
  - Détection des yeux
  - Détection de sourires
  - Détection combinée (visages + yeux + sourires)

- **Reconnaissance faciale personnalisée** :
  - Création de datasets personnalisés
  - Entraînement de modèles de reconnaissance
  - Identification d'individus en temps réel

- **Architecture modulaire** :
  - Scripts séparés pour chaque fonctionnalité
  - Facile à étendre et à maintenir
  - Code réutilisable

## 🏗️ Architecture du Projet

Le projet est structuré en deux modules principaux :

1. **FaceDetection** : Détection en temps réel de caractéristiques faciales
2. **FacialRecognition** : Entraînement et reconnaissance d'identités

## 📦 Prérequis

- Python 3.8 ou supérieur
- Webcam fonctionnelle (pour la détection en temps réel)
- Système d'exploitation : Windows, macOS ou Linux

## 🚀 Installation

1. **Cloner le repository**
git clone https://github.com/votre-username/OpenCV-Face-Recognition.git
cd OpenCV-Face-Recognition

text

2. **Installer les dépendances**
pip install opencv-python
pip install opencv-contrib-python
pip install numpy

text

3. **Vérifier l'installation**
python --version
python -c "import cv2; print(cv2.version)"

text

## 💻 Utilisation

### Détection de Visages

python FaceDetection/faceDetection.py

text

### Détection des Yeux

python FaceDetection/faceEyeDetection.py

text

### Détection de Sourires

python FaceDetection/faceSmileDetection.py

text

### Détection Combinée (Visages + Yeux + Sourires)

python FaceDetection/faceSmileEyeDetection.py

text

### Reconnaissance Faciale Personnalisée

**Étape 1 : Créer un dataset**
python FacialRecognition/01_face_dataset.py

text
Suivez les instructions pour capturer des images de visages.

**Étape 2 : Entraîner le modèle**
python FacialRecognition/02_face_training.py

text

**Étape 3 : Reconnaissance en temps réel**
python FacialRecognition/03_face_recognition.py

text

## 📁 Structure des Fichiers

OpenCV-Face-Recognition/
│
├── FaceDetection/
│ ├── Cascades/
│ │ ├── haarcascade_eye.xml
│ │ ├── haarcascade_frontalface_default.xml
│ │ └── haarcascade_smile.xml
│ │
│ ├── faceDetection.py # Détection de visages
│ ├── faceEyeDetection.py # Détection des yeux
│ ├── faceSmileDetection.py # Détection de sourires
│ └── faceSmileEyeDetection.py # Détection combinée
│
├── FacialRecognition/
│ ├── dataset/ # Images capturées pour l'entraînement
│ ├── trainer/ # Modèles entraînés
│ │
│ ├── 01_face_dataset.py # Création du dataset
│ ├── 02_face_training.py # Entraînement du modèle
│ ├── 03_face_recognition.py # Reconnaissance en temps réel
│ ├── haarcascade_frontalface_default.xml
│ └── FaceRecogBlock.png # Diagramme du système
│
├── README.md
└── requirements.txt

text

## 🛠️ Technologies Utilisées

- **Python 3.8+** : Langage de programmation principal
- **OpenCV 4.x** : Bibliothèque de vision par ordinateur
- **NumPy** : Calcul numérique et manipulation de matrices
- **Cascades de Haar** : Algorithmes de détection d'objets
  - `haarcascade_frontalface_default.xml` : Détection de visages
  - `haarcascade_eye.xml` : Détection des yeux
  - `haarcascade_smile.xml` : Détection de sourires

### Algorithmes de Reconnaissance

Le projet utilise les algorithmes de reconnaissance faciale d'OpenCV :
- **LBPH (Local Binary Patterns Histograms)** : Rapide et efficace
- **EigenFaces** : Basé sur l'analyse en composantes principales
- **FisherFaces** : Analyse discriminante linéaire

## 📸 Exemples

### Détection de Visages
Le système détecte automatiquement les visages dans le flux vidéo et les encadre avec un rectangle vert.

### Reconnaissance Faciale
Une fois entraîné, le système peut identifier des personnes spécifiques et afficher leur nom avec un niveau de confiance.

## 🎯 Cas d'Usage

- Systèmes de sécurité et contrôle d'accès
- Présence automatique dans les salles de classe
- Applications de surveillance
- Interaction homme-machine
- Projets éducatifs en vision par ordinateur

## 🔧 Configuration

### Paramètres de Détection

Vous pouvez ajuster les paramètres de détection dans les scripts :

Paramètres de detectMultiScale
faces = face_cascade.detectMultiScale(
gray,
scaleFactor=1.1, # Facteur d'échelle (1.1 - 1.5)
minNeighbors=5, # Nombre minimum de voisins (3-6)
minSize=(30, 30) # Taille minimale du visage
)

text

## 📝 Notes Importantes

- Pour la reconnaissance faciale, collectez au moins 30-50 images par personne pour de meilleurs résultats
- Assurez-vous d'avoir un bon éclairage lors de la capture d'images
- La webcam doit être autorisée par votre système d'exploitation
- Appuyez sur **'q'** ou **'ESC'** pour quitter les applications

## 🐛 Résolution de Problèmes

**Erreur : Camera not found**
Vérifiez que votre webcam est connectée et autorisée
Essayez de changer l'index de la caméra dans le code
cap = cv2.VideoCapture(0) # Essayez 0, 1, ou 2

text

**Erreur : Cascade file not found**
Vérifiez que les fichiers XML sont dans le bon répertoire
Téléchargez-les depuis le repository OpenCV si nécessaire
text

## 📚 Ressources

- [Documentation OpenCV](https://docs.opencv.org/)
- [Tutoriel Face Recognition OpenCV](https://docs.opencv.org/3.4/da/d60/tutorial_face_main.html)
- [Cascades de Haar](https://github.com/opencv/opencv/tree/master/data/haarcascades)