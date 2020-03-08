---
title: 'Mining, proof of work e creazione di nuovi bitcoin'
subtitle: >-
  Il Mining è il processo tramite il quale nuovi bitcoin sono aggiunti al totale
  di moneta in circolazione.Serve inoltre per proteggere il sistema bitcoin
  contro transazioni fraudolente o transazioni che cercano di spendere lo stesso
  numero di bitcoin più di una volta, problema conosciuto con il nome di
  double-spending (doppia-spesa).I miners provvedono alla potenza di calcolo del
  network bitcoin e come ricompensa per il loro operato ricevono una somma
  prestabilita di bitcoin.Con la potenza di calcolo fornita validano nuove
  transazioni e le registrano sul ledger globale (un libro mastro globale).Un
  nuovo blocco, contenente le transazioni che sono avvenute, è minato (mined) in
  media ogni 10 minuti e aggiunto alle blockchain. Le transazioni che sono
  diventate parte di un blocco e aggiunte alla blockchain sono considerate
  confermate(confirmed), questo permette ai nuovi proprietari dei bitcoin di
  spendere i bitcoin ricevuti nelle suddette transazioni.


  Ogni miner esegue una serie di passaggi che portano a produrre un nuovo
  blocco:


  * Raccoglie e decide quali informazioni, raccolte dalla rete peer-to-peer,
  includere in un nuovo blocco.

  * Verifica che tutte le transazioni che ha incluso nel blocco siano valide.

  * Seleziona il blocco più recente nel ramo più lungo della blockchain e
  inserisce un hash di tale blocco nel nuovo blocco che sta creando.

  * Cerca di risolvere il proof-of-work(spiegazione nello specchietto più in
  basso)per il nuovo blocco e contemporaneamente osserva quali altri nuovi
  blocchi vengono creati da altri nodi.


  Se un miner trova una soluzione al problema della proof of work, il nuovo
  blocco viene aggiunto alla catena e condiviso dalla rete.


  Qualora invece un altro nodo risolvesse prima, il suo blocco verrebbe
  sottoposto ai controlli di validità. Se valido viene aggiunto ad una copia
  locale della BlockChain e condiviso in rete, altrimenti viene scartato.


  La massa monetaria di Bitcoin è creata attraverso questa estrazione (mining)
  nello stesso modo in cui una banca centrale emette nuova valuta.


  La somma di nuovi Bitcoin creati che un miner può estrarre in un blocco
  decresce all’incirca ogni 4 anni (più precisamente ogni 210.000 blocchi). E’
  iniziata con 50 bitcoin per ogni blocco nel Gennaio del 2009 e si è dimezzata
  ogni circa 4 anni fino ad oggi. Si dimezzerà nuovamente tra pochi mesi dalla
  data odierna, verso maggio/giugno del 2020. Le ricompense del mining bitcoin
  scenderanno esponenzialmente fino approssimativamente all’anno 2140 quando
  tutti i bitcoin saranno stati emessi (circa 21 milioni, 20,999 999 98 milioni
  di bitcoin).


  ![](/images/msbt_0801.png)


  Nei 21 milioni sono considerati anche tutti quei bitcoin che sono andati persi
  o resi irrecuperabili per vari motivi come per esempio la perdita della chiave
  privata. In questo caso i bitcoin sono presenti nella blockchain ma sono
  inutilizzabili perché le chiavi private sono andate perdute.


  > Your Keys, Your Bitcoin. Not Your Keys, Not Your Bitcoin cit. Antonopoulos


  I miners nel loro processo di mining ricevono due tipi di ricompense: i
  bitcoin creati ad ogni nuovo blocco e le commissioni (fee) di transazione da
  tutte le transazioni incluse nel blocco.


  Ogni transazione può includere una fee di transazione, nella forma di un
  surplus di bitcoin tra gli input e gli output della transazione.(vedere
  articolo transazioni)


  > dico può ma al momento attuale i miner hanno una politica per la quale le
  transazioni a fee 0 o basse vengono lasciate per ultime e quindi per avere la
  transazione verificata ci vorrà molto tempo con il rischio anche che non entri
  mai a far parte della blockchain.


  Non bisogna però vedere il mining solo come una forma per arricchirsi o solo
  come un processo nel quale la moneta è creata: il mining è il processo
  centrale della Camera di compensazione(clearing house), con il quale le
  transazioni vengono validate ed evase. Il mining protegge il sistema
  bitcoin(da attacchi informatici ecc…) ed abilita l’emergenza di un consenso su
  tutta la rete senza bisogno di un’autorità centrale.


  Il mining è l’invenzione che rende bitcoin speciale, un meccanismo di
  sicurezza che è la base del contante digitale peer-to-peer. La ricompensa per
  le nuove monete coniate e le fee di transazione sono uno schema di incentivi
  che allinea le azioni dei miner con la sicurezza della rete, e simultaneamente
  implementa la fornitura monetaria.


  > Proof of work

  >

  > Il problema della proof of work è un problema crittografico che richiede un
  enorme numero di tentativi e può essere risolto solo tramite il metodo della
  forza bruta(brute force), il quale rende impossibile prevedere quale utente
  troverà la soluzione prima degli altri. Il sistema bitcoin utilizza una
  versione della proof of work chiamata Hashcash, proposta da Adam Back nel
  1997, e sfrutta l’apparente casualità delle funzioni hash. Un algoritmo
  converte un dato arbitrario in un numero esadecimale e, se il dato iniziale
  viene incrementato e ri-sottoposto al calcolo dell’hash, viene prodotto un
  risultato completamente differente. Questa operazione viene eseguita fino a
  che si trova un risultato minore di un valore T, fissato dalla rete. Più
  piccolo è tale valore, più difficile è l’operazione di generazione di un nuovo
  blocco.

  > La soluzione del problema del Proof Of Work si ottiene trovando:

  > X tale che H(x) <=T, dove H rappresenta la funzione hash crittografica.

  >

  > Il protocollo eseguito dai minatori per risolvere il problema è il seguente:

  >

  > * Si incrementa (aumentando di 1 ogni volta) un numero casuale, presente
  nell’intestazione del blocco, che è detto NONCE.

  > * Si esegue un doppio hash SHA256 di alcune parti di blocco chiamati
  nell’insieme, block header.

  >

  > Fra i dati contenuti nel Block Header sono presenti i seguenti valori:

  >

  > * nVersion = numero della versione di Bitcoin utilizzata

  > * HashPrevBlock = hash del blocco precedente

  > * HashMerkle-Root = la radice dell'albero di Merkle a cui fa riferimento il
  blocco

  > * nNonce = valore che viene incrementato ad ogni nuovo tentativo.

  >

  > SHA256^2(block header).

  >

  > * Si verifica che l’hash trovato sia <=T H<=T

  >

  > Se il valore è minore l’utente ha risolto il problema ed il suo blocco viene
  aggiunto alla catena, in caso contrario il blocco viene rifiutato dal sistema
  e ricomincia la prova da punto 1).


  ![](/images/What-is-proof-of-workITA.jpg)


  Risolvere il problema del Proof Of Work non comporta solo una spesa di tempo,
  ma anche di elettricità, che permettere ai computer di elaborare il problema e
  svolgere continuamente dei calcoli. Per invogliare gli utenti a utilizzare i
  propri calcolatori per validare i blocchi, il sistema Bitcoin elargisce una
  certa quantità di BTC a chi produce un blocco valido.


  > Transazione Coinbase

  >

  > Una transazione Coinbase, cosiddetta “di Generazione”, è la prima che viene
  inclusa in un blocco nel momento della sua creazione, ed è utilizzata per
  pagare una ricompensa ai minatori che per primi risolvono il Proof Of Work.
  Tale transazione viene aggiunta come prima transazione in ogni blocco e i
  miners la inseriscono così da auto premiarsi. Infatti, nell’output delle
  transazioni coinbase si trovano gli indirizzi specifici dei miners che hanno
  convalidato i blocchi e che, di conseguenza, hanno ricevuto la ricompensa.

  >

  > Tale transazione ha come input un valore casuale che il minatore può
  utilizzare come valore nonce, come output il valore null, nel campo prevout,
  perché non fa riferimento ad alcuna transazione precedente, e uno o più
  indirizzi a cui, nel caso in cui il blocco sia accettato nella catena di
  blocchi, viene assegnata l'intera somma o parte di essa.


  Una transazione Coinbase non trasferisce bitcoin, bensì ne crea di nuovi:
  questo è anche l'unico modo per far entrare in circolazione nella rete nuovi
  bitcoin.


  Quindi, ricapitolando, il mining è il processo che serve a rendere sicuro il
  sistema bitcoin, a validare le transazioni ed “emettere” nuovi bitcoin. I
  miners, coloro che effettuano l’operazione di mining, devono competere nel
  risolvere un difficile problema matematico basato su un algoritmo
  crittografico detto proof of work: la soluzione a questo problema è inclusa
  nel nuovo blocco e agisce come prova che il miner ha impegnato uno sforzo
  computazionale adeguato. Questa “gara” per risolvere l’algoritmo di proof of
  work per ottenere la ricompensa e il diritto di registrare le transazioni
  nella blockchain è alla base del modello di sicurezza di bitcoin.


  La DIFFICULTY


  La difficoltà della Proof of work è regolata in modo da limitare la velocità
  con cui i nuovi blocchi possono essere generati dalla rete, e quindi aggiunti
  alla Blockchain: è importante che i nuovi blocchi non siano generati troppo
  velocemente o troppo lentamente.


  Se i blocchi fossero creati troppo velocemente la BlockChain conterrebbe molte
  biforcazioni, che renderebbero difficoltosa ai nodi la scelta del ramo su cui
  lavorare. D'altra parte se la creazione fosse troppo lenta ci vorrebbe molto
  tempo per confermare le transazioni.


  I nodi del sistema Bitcoin si servono del target T per regolare
  automaticamente la velocità di creazione dei blocco, in modo che occorra ogni
  volta una media di 10 minuti affinché ne venga creato uno nuovo.


  Il target è un numero a 256-bit condiviso da tutti i client. Il target massimo
  usato da Bitcoin è


  0x00000000FFFF0000000000000000000000000000000000000000000000000000,


  questo valore rappresenta la più bassa difficoltà di creazione di un blocco
  che si può riscontrare.


  La difficulty D è una misura di quanto sia difficile, dal punto di vista
  computazionale, trovare un valore di hash minore di un fissato valore target.
  E’ definita come il rapporto fra il massimo numero target possibile e il
  target corrente.


  D= T<sub>max</sub>/T


  > Modifica Difficulty

  >

  > La difficulty viene modificata ogni 2016 blocchi creati (circa ogni 2
  settimane), e si basa sul tempo medio usato per creare l’ultimo blocco. Poiché
  ogni valore hash è un numero di 256bit, vi sono 2<sup>256</sup> possibili
  valori hash e dunque la probabilità di trovare un valore hash minore di T in
  una sola volta è:

  >

  > p(T)= T/2<sup>256</sup>

  >

  > quindi il numero di prove necessarie a trovarlo sarà in media:

  >

  > N(T)= 1/p(T) = 2<sup>256</sup>/T

  >

  > Se gli ultimi 2016 blocchi sono stati generati in un tempo di circa tm, con
  un target di T, allora possiamo stimare che i miners collettivamente hanno ad
  una velocità di:

  >

  > v=N(T)/tm

  >

  > il tempo previsto per creare un blocco, con difficoltà T e velocità di hash
  v è allora:

  >

  > t(T,r)=N(T)/v

  >

  > il valore target deve quindi essere regolato ad una valore T’ così che
  t(T’,v)=600sec ovvero 10 min

  >

  > 600sec= t(T’,v) = N(T’)/v = N(T’)/(N(T)/tm) = tm*(T/T’)

  >

  > Da cui: T’=(tm/600)T.)


  In questo articolo abbiamo spiegato brevemente il processo che consente di
  validare le transazioni emesse, costituendo il pilastro alla base
  dell’affidabilità di Bitcoin ed il meccanismo di creazione di nuove monete.
date: 2020-01-25T21:11:27.862Z
layout: page
---
