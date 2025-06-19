#enoncé
Sujet : Prévision des délais de livraison ou des retards (ETA prediction) pour une chaîne logistique (e-commerce, transport, ou distribution industrielle).
file name: "supply_chain_large.csv"
    Machine learning:
Nettoyage de la donnée
Une fois rassemblées, les données peuvent avoir besoin d'être nettoyées. Caractères spéciaux, données manquantes, hétérogénité de la casse : tous ces cas de figure peuvent être un frein à la modélisation de nos données.

    Encodage
Les données à disposition ne sont pas toujours des données numériques : type catégoriel, textuel ou encore date, tous ces types de données nécessitent un traitement particulier pour les convertir en valeurs numériques car les algorithmes de Machine Learning prennent en entrée uniquement des valeurs numériques. Ce format de données est donc indispensable pour leur bon fonctionnement.

    Transformation
L'application de certains algorithmes de Machine Learning nécessite la vérification d'un ensemble d'hypothèses. Pour respecter ces hypothèses, il est souvent nécessaire d'appliquer des transformations à nos variables. On pourra par exemple citer la transformation logarithmique, la standardisation ou encore la normalisation. Il est à noter que tous les algorithmes n'ont pas besoin des mêmes traitements. Les modèles linéaires ou plus globalement ceux qui font intervenir la notion de distance sont souvent très sensibles à ces transformations qui vont alors être très importantes pour leur bon fonctionnement. En particulier, la mise à l'échelle des variables sera indispensable avant d'entraîner un modèle linéaire.

#architecture projet
supply-chain-mlops/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   └── serving/
├── tests/
├── mlruns/ (si MLflow)
├── Dockerfile
├── requirements.txt
├── dvc.yaml (optionnel)
└── README.md
#création d'environnement virtuel
    python -m venv supply_ops
    source supply_ops/Scripts/activate
réduction de la ligne du terminal 
    PS1=">"
mettre à niveau "pip"
    python.exe -m pip install --upgrade pip
