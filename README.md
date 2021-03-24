# Préparation d'images dans le cloud

Ce projet utilise les données disponibles à [cette adresse](https://www.kaggle.com/moltean/fruits).  
Il consiste à préparer ce jeux de données avant de l'utiliser pour entraîner un modèle de reconnissance automatique de fruits à partir des images dans le cloud.  
Les images de 100x100 px sont étiquetées avec la variété de fruit puis converties en un tableau de 30 000 valeurs, puis une analyse en 50 composantes principales 
permet de réduire le nombre de dimensions tout en conservant la grande majorité de variance expliquée.  

Le notebook présente l'ACP sur un échantillon à partir de laquelle le choix de 50 composantes principales est retenu.  
Le programme d'amorçage et le programme de traitement des images en clacul distribué (Spark) y sont présentés ensuite.  
Ces programmes ont tourné sur un cluster EMR de AWS lié à un stockage S3. 
Ce stockage S3 est public et accessible à l'adresse https://samuel-pate-projet-8.s3.us-east-2.amazonaws.com/.
