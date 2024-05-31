<img width="1392" alt="Capture d’écran 2024-05-29 à 17 54 41" src="https://github.com/telecom-business-finance/qrt-datachallenge/assets/85460872/ccd44a8c-8ea5-4822-a0a8-1bd5c49d939a">

# QRT Datachallenge Setup Guide

Ce guide vous aidera à configurer votre environnement de développement pour travailler avec Jupyter Notebook sur Visual Studio Code (VSCode), que vous soyez sur macOS ou Windows. Vous aurez également la possibilité de créer un environnement Conda ou non.

## Prérequis

- [Visual Studio Code](https://code.visualstudio.com/)
- [Python](https://www.python.org/downloads/) (version 3.7 ou supérieure)

## Installation de Conda (optionnel)

Conda est un gestionnaire d'environnements et de packages pour Python. Il est recommandé mais pas obligatoire. Vous pouvez l'installer en suivant les étapes ci-dessous.

### Installation de Conda

#### macOS

1. Téléchargez l'installateur de Miniconda depuis [ce lien](https://docs.conda.io/en/latest/miniconda.html) pour macOS.
2. Ouvrez le terminal et exécutez le script d'installation :
    ```bash
    bash Miniconda3-latest-MacOSX-x86_64.sh
    ```
3. Suivez les instructions à l'écran pour compléter l'installation.
4. Fermez et rouvrez votre terminal pour activer Conda.

#### Windows

1. Téléchargez l'installateur de Miniconda depuis [ce lien](https://docs.conda.io/en/latest/miniconda.html) pour Windows.
2. Exécutez l'installateur et suivez les instructions à l'écran.
3. Redémarrez votre terminal ou invite de commande pour activer Conda.

### Création d'un environnement Conda

1. Ouvrez votre terminal (macOS) ou invite de commande (Windows).
2. Créez un nouvel environnement Conda avec Python 3.11 :
    ```bash
    conda create --name datachallenge python=3.11
    ```
3. Activez l'environnement :
    ```bash
    conda activate datachallenge
    ```

## Installation de Jupyter Notebook et autres packages

Que vous utilisiez Conda ou non, suivez ces instructions pour installer les packages nécessaires.

### Avec Conda

1. Installez Jupyter Notebook et d'autres packages :
    ```bash
    conda install ipykernel jupyter pandas numpy matplotlib scikit-learn
    ```

### Sans Conda

1. Assurez-vous que pip est installé. Vous pouvez vérifier cela en exécutant :
    ```bash
    python -m pip --version
    ```
2. Installez Jupyter Notebook et d'autres packages :
    ```bash
    pip install ipykernel jupyter pandas numpy matplotlib scikit-learn
    ```

## Configuration de VSCode

1. Ouvrez VSCode.
2. Installez l'extension **Python** de Microsoft. Vous pouvez la trouver dans le Marketplace de VSCode.
3. Installez l'extension **Jupyter** de Microsoft.
4. Ouvrez le dossier ou le répertoire de votre projet dans VSCode.
5. (Optionnel) Si vous utilisez Conda, sélectionnez votre environnement Conda :
    - Cliquez sur l'icône en bas à gauche de VSCode indiquant la version de Python.
    - Sélectionnez votre environnement `datachallenge`.

## Test de la configuration

1. Créez un nouveau fichier Jupyter Notebook en cliquant sur l'icône **New File** puis en sélectionnant **Jupyter Notebook**.
2. Dans la première cellule, collez le code suivant et exécutez la cellule :

    ```python
    import pandas as pd
    import numpy as np
    import matplotlib.pyplot as plt
    import sklearn

    # Vérification des versions
    print(f"Pandas version: {pd.__version__}")
    print(f"NumPy version: {np.__version__}")
    print(f"Matplotlib version: {plt.__version__}")
    print(f"Scikit-learn version: {sklearn.__version__}")

    # Test de l'affichage graphique
    plt.plot([1, 2, 3], [4, 5, 6])
    plt.title("Test Plot")
    plt.show()
    ```

Si tout fonctionne correctement, vous devriez voir les versions des packages installés et un graphique simple.
