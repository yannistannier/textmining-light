### Sujet 4. Reconnaissance d'entités nommées avec Spacy

L’objectif est d’entrainer un modele Spacy a reconnaitre deux types d’entite biomedicales (GENE, DISEASE) au sein de textes.


Tester le model : http://textmining.yannistannier.io


Meilleur model (en ligne sur le site) : fs_normal/best_model

Meilleur model sur NBCICorpus : fs_normal_nbci/epoch_71_best_model


### Presentation code : 

Repertoires : 

- data_aggregation => contient tout le code qui nous a permis de collecter les genes/maladies

- train => contient les données d'entraintement (supprimé dans ce depot mais qui être reproduit facilement en executant le code dans create_dataset.ipynb)

- test => contient les données de test

- models => contient les models (fs_normal = model entrainé uniquement sur les données autism / asthma,  fs_normal_ncbi = model entrainée sur autism/asthm + NCBICorpus et juste NCBICorpus )

Scripts : 

- creata_dataset.ipynb => Script de creations des different dataset (train/test)

- train_fromscratch.py => script pour le training des models

- eval_ner.ipynb => scritp des differents evaluation des models

- api.py => permet de faire tourner l'api de prediction pour le site

Fichiers : 

- list_genes.text => Fichier final contenant tous les genes (obtenu grace aux codes du repertoire "data_aggregation" )

- list_maladies.text => Fichier final contenant toutes les maladies (obtenu grace aux codes du repertoire "data_aggregation" )

- NBCItestset_corpus.txt => Fichiers des données de test de NBCICorpus (avant traitement) 

- NBCItrainset_corpus.txt => Fichiers des données de train de NBCICorpus (avant traitement) 