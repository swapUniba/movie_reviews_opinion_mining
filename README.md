# tesi_itps

## Contenuto del repository
Notebook:
* reviews_mapping.ipynb: script per l'elaborazione del dataset di recensioni allo scopo di renderlo compatibile con lo script opinion_mining.ipynb. Richiede il dataset contenente le recensioni: https://unibari-my.sharepoint.com/:u:/g/personal/cataldo_musto_uniba_it/EUbztek47bRMtkvsmb-a59IBH9i_qY0GV1VZdEibTU3rQw?e=Ggh45j;
* opinion_mining.ipynb: script per l'estrazione di aspetti a partire da testo user-generated. Richiede:
  * dataset pre-elaborato: https://drive.google.com/file/d/1VQvjvRcL1rkHiv9Aq0WdsVloGtV9eRoe/view?usp=sharing;
  * cartella stopwords;
  * dataset_movie_list.txt;
  * reviewsPerFilm.txt;
* experiment_results: script per la visualizzazione dei risultati della sperimentazione.

File:
* stopwords: cartella contenente i file con le stop words utilizzate da opinion_mining.ipynb;
* dataset_movie_list.txt: lista di ID dei film contenuti nel dataset con le recensioni, utilizzata da opinion_mining.ipynb (è possibile generare questo file utilizzando reviews_mapping.ipynb);
* reviewsPerFilm.txt: lista contenente il numero di recensioni contenute nel dataset per ogni film, utilizzata da opinion_mining.ipynb (è possibile generare questo file utilizzando reviews_mapping.ipynb).

## Istruzioni
### opinion_mining.ipynb
Scaricare il contenuto del repository.\
Aprire Colab e caricare il notebook opinion_mining.ipynb.\
Caricare in una cartella in Google Drive i file dataset_movie_list.txt, reviewsPerFilm.txt, la cartella stopwords e il contenuto del dataset pre-elaborato: è necessaria solo la cartella splitted_dataset. splitted_sentiment e splitted_processed_tokens sono utili solo per evitare di dover eseguire la fase di Pre-processing. Se si vuole solo effettuare la fase di Aspect Extraction e Aspect Selection basta caricare solo splitted_processed_tokens.\
Settare opportunamente le celle nel blocco Setup ed eseguire tutte le celle nel blocco Setup e nel blocco Funzioni.\
Eseguire tutte le celle nei blocchi Pre-processing, Aspect Extraction e Aspect Selection se si vuole eseguire tutta la pipeline a partire dai file in splitted_dataset, altimenti eseguire solo le celle nei blocchi Aspect Extraction e Aspect Selection se si vuole eseguire la pipeline a partire dai file in splitted_processed_tokens.\
N.B. se si vuole eseguire la fase di Pre-processing è opportuno utilizzare una Runtime provvista di GPU. È possibile farlo dal menu Runtime -> Cambia tipo di runtime -> Accelerazione hardware -> GPU.
