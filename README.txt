Binôme :
- Eldis YMERAJ #22408331
- Redwan OMARI #22406817

Partie ETL(dossier projet_hop) :

Cette partie se trouve dans le dossier projet_hop/projet_hop. Vous y trouverez le fichier datawarehouse.txt qui nous a permis de créer nos tables avec SQLite3 et de les alimenter grâce à Apache Hop.

Organisation des fichiers dans le répertoire :
- datawarehouse.txt : Fichier de requêtes SQL pour la création des tables.
- Pipeline ETL :
  - pipeline1.hpl, pipeline2.hpl, pipeline3.hpl : Les pipelines Hop utilisés pour l'alimentation des données dans l'entrepôt de données.
- Dossier data_in : Contient les fichiers d'entrée qui ont servi à alimenter l'entrepôt de données :
  - dates.csv
  - geographie.csv
  - operational_data.db
  - prestations.csv
- Dossier data_out : Contient les fichiers de sortie après le traitement :
  - datawarehouse.db : La base de données de l'entrepôt de données final.
  - Errors.csv.txt : Fichier d'erreurs rencontré pendant le traitement.
  
Dans le répertoire principal projet_hop, vous trouverez également le fichier diagramme.png qui représente le diagramme sur lequel nous nous sommes basés pour créer l'entrepôt de données. Pour plus de détails, regardez le rapport.


Partie Cube(dossier tp_olap) :

Nous avons mis en place une copie de notre datawarehouse.db dans le dossier tp_olap/datawarehouse. 

Le schéma XML se trouve dans le dossier exercices avec toutes les requêtes MDX demandées. Chaque requête MDX est dans un fichier différent (`ex2.mdx`, `ex3.mdx`, ..., `ex11.mdx`), ce qui permet d'exécuter les requêtes exercice par exercice.

Instructions pour exécuter les requêtes MDX :

1. Se rendre dans le répertoire `tp_olap`.
2. Exécuter la commande suivante pour chaque requête MDX(en fonction de l'exercice(ex2.mdx jusqu'a ex11.mdx) :
sh run.sh -p exercices/exercice.properties -f exercices/ex9.mdx | java -jar lib/mondrian_view.jar

Il y a un total de 10 requêtes MDX à exécuter : `ex2.mdx`, `ex3.mdx`, ..., `ex11.mdx`.
