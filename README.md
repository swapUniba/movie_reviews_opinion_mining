# tesi_itps

## Contenuto del repository
Notebook:
* reviews_mapping.ipynb: script per l'elaborazione del dataset di recensioni allo scopo di renderlo compatibile con lo script opinion_mining.ipynb. Richiede il dataset contenente le recensioni: ;
* opinion_mining.ipynb: script per l'estrazione di aspetti a partire da testo user-generated. Richiede:
  * dataset pre-elaborato: (necessaria solo la cartella splitted_dataset, splitted_sentiment e splitted_processed_tokens sono utili solo per evitare di dover eseguire la fase di Pre-processing);
  * cartella stopwords;
  * dataset_movie_list.txt;
  * reviewsPerFilm.txt;
* experiment_results: script per la visualizzazione dei risultati della sperimentazione.

File:
* stopwords: cartella contenente i file con le stop words utilizzate da opinion_mining.ipynb;
* dataset_movie_list.txt: lista di ID dei film contenuti nel dataset con le recensioni, utilizzata da opinion_mining.ipynb (è possibile generare questo file utilizzando reviews_mapping.ipynb);
* reviewsPerFilm.txt: lista contenente il numero di recensioni contenute nel dataset per ogni film, utilizzata da opinion_mining.ipynb (è possibile generare questo file utilizzando reviews_mapping.ipynb).

Il dataset 
