Achraf HAMSI/Projet DE #3 - Base de données & API de données// 
L’objectif de ce projet est de choisir, mettre en place, et peupler une base de données SQL à partir d’un jeu de données de l’open data, et d’implémenter une API vous permettant de requêter cette base de données.

Le jeu de données est sous format CSV et peut etre récupéré dans le repository du projet ou via ce lien: https://www.kaggle.com/syedjaferk/book-crossing-dataset?select=BX-Books.csv

La base de données créée à l'aide du ficher create_bdd.py est également disponible dans le repository.

Les étapes du projet sont:
1) Création de la base de données. Pour cela:
    - Le script est dans le fichier create_bdd.py
    - Création de l'image à l'aide du fichier DockerFile_create_db : 
       command : docker image build . -t projet:latest --file ./DockerFile_create_db
    - copier la base de données du container ou lancer le fichier create_bdd.py avec la commande suivante : python3 create_bdd.py pour créer la bdd_datascientest_projet3.dd dans répertoire du projet 3

2) Test et requete de la base de données localement. Pour cela:
    - Le script est dans le fichier test_db.py
    - Création de l'image à l'aide du fichier DockerFile_test_db
    - Lancement du conteneur avec le docker compose
       command : docker-compose up
    - Ceci affichera les resultats des requetes directement dans le terminal

3) Création de l'API pour rendre la base de données accessible depuis l'interface Web de l'API. Pour cela:
    - Le script est dans le fichier api.py
    - Création de l'image à l'aide du fichier DockerFile_api
    - Lancement du conteneur avec le docker compose
       command : docker-compose up
    - Ceci lancera l'API dans le localhoste port 5010# Base-de-donn-es-SQL-API-de-donn-es
