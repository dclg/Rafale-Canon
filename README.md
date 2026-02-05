# Canon Burst Extractor

Ce script Python permet d'extraire les images individuelles (RAW CR3 et JPEG) à partir d'un fichier de "rafale" Canon (Burst file). Il est conçu pour fonctionner avec les fichiers générés par certains appareils Canon qui groupent les prises de vue en rafale dans un seul conteneur.

## Fonctionnalités

*   Extraction des prévisualisations JPEG.
*   Reconstruction des fichiers RAW `.CR3` originaux.
*   Support des templates intégrés ou externes pour la reconstruction des entêtes CR3.
*   Interface graphique (GUI) simple pour sélectionner des fichiers ou des dossiers.
*   Utilisable également en ligne de commande.

## Prérequis

*   Python 3.x
*   Les dépendances listées dans `requirements.txt` (principalement pour la création de l'exécutable).

## Installation

1.  Clonez ce dépôt ou téléchargez les fichiers.
2.  Installez les dépendances nécessaires (si vous souhaitez compiler) :
    ```bash
    pip install -r requirements.txt
    ```

## Utilisation

### Ligne de commande

Vous pouvez lancer le script en lui passant un fichier ou un dossier en argument :

```bash
python canon_burst_extractor.py "C:\Chemin\Vers\Fichier.CR3"
```
ou
```bash
python canon_burst_extractor.py "C:\Chemin\Vers\Dossier"
```

### Interface Graphique

Si vous lancez le script sans argument, une fenêtre s'ouvrira vous demandant de choisir entre traiter un fichier unique ou un dossier complet.

```bash
python canon_burst_extractor.py
```

## Création de l'exécutable (Windows)

Pour créer un exécutable autonome `.exe` :

1.  Assurez-vous d'avoir installé `pyinstaller` :
    ```bash
    pip install pyinstaller
    ```
2.  Lancez la commande de build :
    ```bash
    pyinstaller --onefile --windowed --name "CanonBurstExtractor" canon_burst_extractor.py
    ```
    L'exécutable sera généré dans le dossier `dist/`.

## Téléchargement

📥 **Télécharger la dernière version (Windows .exe) :** [CanonBurstExtractor v1.0.0](https://github.com/dclg/Rafale-Canon/releases/tag/v1.0.0)


## Avertissement Légal

Ce logiciel est un outil d'ingénierie inverse développé indépendamment. Il n'est ni affilié, ni autorisé, ni approuvé par Canon Inc. Le format de fichier CR3 est la propriété de Canon. Cet outil est fourni à des fins d'interopérabilité et d'éducation.
