# DigiamoProject
test di valutazione

In questo progetto ho innanzitutto fatto un analisi del dataset fornito. Dal dataset si evince che ci sono 21 classi diverse di output. Il Dataset ha circa 320 mila row. Non è bilanciato come si vede:
mainichi.jp          44657
sankei.jp.msn.com    35959
nikkei.com           29323
sanspo.com           26303
tomamin.co.jp        26054
nikkansports.com     25483
oita-press.co.jp     23645
yomiuri.co.jp        22472
nishinippon.co.jp    21311
asahi.com            19855
hokkaido-np.co.jp    10653
shimotsuke.co.jp      9581
kobe-np.co.jp         8311
kyoto-np.co.jp        3408
yamagata-np.jp        2585
isenp.co.jp           1496
iwate-np.co.jp        1198
nnn.co.jp              347
tokachi.co.jp          176
chunichi.co.jp          73
tokyo-np.co.jp          65


Ho provato sia tecniche utilizzando modelli di ML come RandomForrest, SVM che tecniche di deep learning in cui dopo vari tentativi ho trovato una rete convoluzionale che performa abbastanza per bene per questa tipologia di task. Ho provato a fare fine-tuning dei  parametri utilizzando varie  tipologie di tuner tra cui RansomSearch, BayesianOptimization e Hyperband per trovare i migliori iperparametri dei vari layer della rete. Ho usato anche come approccio il trasnfer+learning utilizzando una rete molto utilizzata con i linguaggi(BERT) e per bilanciare il dataset ho provato anche tecniche come oversampling e dato pesi diversi alle varie classi inversamente proporziale al numero di elementi per ogni output.


Il grosso limite riscontrato è che non avendo gli strumenti per esereguire il mio notebook tranne colab che richiede troppo tempo e il bisogno di essere sempre attivo per eseguire il notebook o kaggle che permette di usare 30 ore settimananali di GPU non ho potuto eseguire il notebook per tante epoch soprattutto anche con il fine tuning dato che oltre le 12 ore per notebook il calcolo viene bloccato.Dai risultati ottenuti utilizzando solo una parte del dataset sono riuscito ad ottenere circa 0.57 come accuracy nel calidation set. 

