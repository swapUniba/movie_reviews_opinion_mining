# movie_reviews_opinion_mining

## Contenuto del repository
Notebook:
* _reviews_mapping.ipynb_: notebook per l'elaborazione del dataset di recensioni allo scopo di renderlo compatibile con lo script _opinion_mining.ipynb_. Richiede il dataset contenente le recensioni: https://unibari-my.sharepoint.com/:u:/g/personal/cataldo_musto_uniba_it/EUbztek47bRMtkvsmb-a59IBH9i_qY0GV1VZdEibTU3rQw?e=Ggh45j;
* _opinion_mining.ipynb_: notebook per l'estrazione di aspetti a partire da testo user-generated. Richiede:
  * dataset pre-elaborato: https://drive.google.com/file/d/1VQvjvRcL1rkHiv9Aq0WdsVloGtV9eRoe/view?usp=sharing;
  * cartella _stopwords_;
  * _dataset_movie_list.txt_;
  * _reviewsPerFilm.txt_;
* _experiment_results_: notebook per la visualizzazione dei risultati della sperimentazione.

File:
* _stopwords_: cartella contenente i file con le stop words utilizzate da _opinion_mining.ipynb_;
* _dataset_movie_list.txt_: lista di ID dei film contenuti nel dataset con le recensioni, utilizzata da _opinion_mining.ipynb_ (è possibile generare questo file utilizzando _reviews_mapping.ipynb_);
* _reviewsPerFilm.txt_: lista contenente il numero di recensioni contenute nel dataset per ogni film, utilizzata da _opinion_mining.ipynb_ (è possibile generare questo file utilizzando _reviews_mapping.ipynb_).

## Istruzioni
### Estrazione degli aspetti
Scaricare il contenuto del repository.\
Aprire Colab e caricare il notebook _opinion_mining.ipynb_.\
Caricare in una cartella in Google Drive i file _dataset_movie_list.txt_, _reviewsPerFilm.txt_, la cartella _stopwords_ e il contenuto del dataset pre-elaborato: è necessaria solo la cartella _splitted_dataset_. _splitted_sentiment_ e _splitted_processed_tokens_ sono utili solo per evitare di dover eseguire la fase di Pre-processing. Se si vogliono eseguire solo le fasi di Aspect Extraction e Aspect Selection basta caricare _splitted_processed_tokens_.\
Settare opportunamente le celle nel blocco Setup ed eseguire tutte le celle nel blocco Setup e nel blocco Funzioni.\
Eseguire tutte le celle nei blocchi Pre-processing, Aspect Extraction e Aspect Selection se si vuole eseguire tutta la pipeline a partire dai file in _splitted_dataset_, altimenti eseguire solo le celle nei blocchi Aspect Extraction e Aspect Selection se si vuole eseguire la pipeline a partire dai file in _splitted_processed_tokens_.\
__N.B.__ se si vuole eseguire la fase di Pre-processing è opportuno utilizzare una Runtime provvista di GPU. È possibile farlo dal menu Runtime -> Cambia tipo di runtime -> Accelerazione hardware -> GPU.

### Esecuzione completa a partire da un nuovo dataset
Utilizzare il notebook _reviews_mapping.ipynb_, adattando il codice nella cella "Mapping dei film in _idMapping.txt_ con le review" in base alle caratteristiche del dataset utilizzato (il codice presente funziona solo con il dataset https://unibari-my.sharepoint.com/:u:/g/personal/cataldo_musto_uniba_it/EUbztek47bRMtkvsmb-a59IBH9i_qY0GV1VZdEibTU3rQw?e=Ggh45j).\
Successivamente utilizzare il notebook _opinion_mining.ipynb_ per estrarre gli aspetti.
