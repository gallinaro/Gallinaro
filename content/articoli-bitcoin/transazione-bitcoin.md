---
title: Transazione bitcoin
subtitle: >-
  Il sistema bitcoin, al contrario dei tradizionali sistemi bancari e dei
  sistemi di pagamento, è basato sulla decentralizzazione della fiducia. Invece
  di un’autorità centrale fiduciaria, in bitcoin, la fiducia si ottiene come
  proprietà emergente dall’integrazione di diversi partecipanti nel sistema
  bitcoin. Questo sistema permette di eliminare le terze parti, i mediatori e
  consente di emanciparci dall’odierno sistema centralizzato di sistemi bancari
  e di pagamento, permettendo da un lato di renderci più autonomi ma dall’altro
  ci costringe a diventare più consapevoli e responsabili nella gestione dei
  nostri fondi.Prendendo spunto da Andreas M. Antonopoulos in questo articolo
  esamineremo il bitcoin “da lontano”, seguendo la singola transazione
  attraverso il sistema bitcoin.


  **Introduzione**


  Il sistema bitcoin consiste principalmente in:


  * Utenti con portafogli (wallet) contenenti chiavi (key)\

  * Transazioni  propagate attraverso la rete\

  * Miner che producono, attraverso una gara di computazione, la blockchain,
  cioè il libro mastro di tutte le transazioni


  Per questo articolo ci soffermeremo ad un livello abbastanza alto esaminando
  come la singola transazione viaggia attraverso il network e come questa
  interagisca col sistema.Simuliamo una compravendita di un bene (bilanciere) in
  un piccolo negozio di paese che ha da poco iniziato ad accettare bitcoin. I 2
  soggetti interessati sono Marco e Giovanni.

  Marco ha appena comprato dei bitcoin che ha successivamente spostato nel suo
  wallet che ora contiene 0.1 BTC.

  Ora Marco può effettuare la sua prima transazione nel negozio di Giovanni.

  Il POS di Giovanni,arrivato il momento di pagare,converte il prezzo da euro a
  bitcoin mostrando a Marco i valori in entrambe le valute. Mostrerà poi un QR
  code contenente una richiesta di pagamento per la transazione.


  * Un QR code di un normale wallet non è nient’altro che la conversione “in
  figura” della chiave pubblica di un wallet: potremmo paragonare questa chiave 
  all’IBAN del nostro conto corrente.\

  * Il QR code di Giovanni, essendo una richiesta di pagamento (payment
  request), contiene la chiave pubblica di Giovanni, il valore del pagamento, e
  una descrizione generica come “negozio Giovanni”.


  Questo consente ad un’applicazione wallet bitcoin di precompilare le
  informazioni usate per inviare il pagamento e allo stesso tempo mostrare
  all’utente una descrizione leggibile dell’operazione.

  Marco usa il suo Iphone per scansionare il QR code così facendo il suo iphone
  mostra a schermo un pagamento di 0.015 BTC verso il negozio di Giovanni, a
  questo punto Marco non dovrà far altro che selezionare a schermo "invia" così
  da autorizzare la transazione.

  Pochi istanti dopo Giovanni è in grado di vedere la transazione ed in questo
  momento la transazione è completata.

  Le transazioni sono come righe in un registro di contabilità in partita
  doppia. Ogni transazione è una serie di input e output, che non sono altro che
  i crediti e debiti.


  ![](/images/libromastro-bitconi.png)


  **Le transazioni**


  L’idea generale delle transazioni nel network bitcoin è quella di inviare
  degli input che vanno a spendere degli output. Ogni transazione ha quindi
  almeno un input ed un output. Ogni input spende un output precedente.

  Ciascun output è quindi una specie di “sala di attesa” che prende il nome di
  output non speso (Unspent Output), finché un successivo input non lo “spende”.

  Ogni transazione ha come prefisso il numero della versione, che ha lo scopo di
  indicare agli altri peers ad ai miners il corretto insieme di regole da usare
  per validarla. Questo dà la possibilità agli sviluppatori di poter creare
  nuove regole senza invalidare le transazioni precedenti.


  Ogni output ha un numero (output index) basato sul suo posto nella
  transazione(il primo avrà come indice 0, il secondo 1 e così via..). Inoltre
  nell’output è presente la quantità di satoshi, che viene pagata ad una chiave
  pubblica che conferma le condizioni di spesa specificate (PublicKey Script).


  D’altro canto, un input utilizza un numero di identificazione della
  transazione (Transaction Identifier-TxId) ed un numero di indice dell’output,
  che serve ad identificare precisamente quale output debba essere speso.
  Inoltre, nell’input è presente uno script di firma (Signature script)
  all’interno del quale sono contenute informazioni e parametri che debbono
  soddisfare le condizioni di spesa indicate nel PubKey Script.


  ![](/images/reansazione-bitcoin.png)


  Quindi Marco invia una transazione a Giovanni, che successivamente la spende.

  Il formato di transazione più comune è chiamato Pay-To-Public-Key-Hash
  (P2PKH).

  Questo sistema utilizza una tecnica crittografica basata su un paio di chiavi,
  la chiave pubblica (public key) e la chiave privata (private key). 


  > La chiave pubblica è da intendere come un IBAN e viene quindi condivisa per
  indicare l’indirizzo dove si vogliono ricevere le transazioni; mentre la
  chiave privata è da intendere come una password e deve quindi rimanere
  segreta, pena la possibilità di perdere i propri fondi contenuti all’interno
  del wallet corrispondente.


  Per creare la prima transazione, Giovanni deve quindi generate un paio di
  chiavi pubblica/privata (bitcoin utilizza l’algoritmo ECDSA con la curva
  secp256k1). Una copia di queste informazioni è quindi trasformata
  deterministicamente in una chiave pubblica secp256k1.

  Tramite l’utilizzo di una tecnica crittografia chiamata hashing, la chiave
  pubblica (PubKey) è quindi “offuscata” e trasformata in una stringa
  alfanumerica univoca. Il processo di hashing è unidirezionale non reversibile,
  pertanto non è possibile eseguire l’operazione inversa per derivare la chiave
  privata di Giovanni.

  Giovanni invia quindi l’hash della sua chiave pubblica a Marco, sotto forma di
  un indirizzo bitcoin.

  Una volta ricevuto l’hash della chiave pubblica di Giovanni, Marco utilizza
  l’hash per creare la sua prima transazione. Viene quindi creato un Output
  P2PKH standard, indicando le istruzioni che danno la possibilità a chiunque di
  spendere l’output nel caso in cui controllino la chiave privata corrispondente
  all’hash della chiave pubblica fornita da Giovanni.

  Queste istruzioni sono contenute nel PubKey Script.

  Marco trasmette quindi la transazione sulla blockchain; il network la
  categorizza come un Output Non Speso e il wallet di Giovanni come saldo
  spendibile.

  Così facendo Marco trasmetterà la transazione ai miner bitcoin, tramite il
  network peer-to-peer. Ogni peer e miner validerà indipendentemente la
  transazione, prima di includerla in un nuovo blocco di transazioni.


  Tranquillizzo tutti spiegando che tutti questi passaggi sono fatti
  autonomamente dal wallet utilizzato:l’utente finale non dovrà fare nulla di
  complicato. Una transazione bitcoin ai suoi occhi sembrerà paragonabile ad una
  transazione fatta con una qualsiasi carta di credito.
excerpt: >-
  Il sistema bitcoin, al contrario dei tradizionali sistemi bancari e dei
  sistemi di pagamento, è basato sulla decentralizzazione della fiducia. Invece
  di un’autorità centrale fiduciaria, in bitcoin, la fiducia si ottiene come
  proprietà emergente dall’integrazione di diversi partecipanti nel sistema
  bitcoin.
img_path: ''
post_button_label: Leggi
date: 2019-10-10T22:00:00.000Z
layout: page
---

