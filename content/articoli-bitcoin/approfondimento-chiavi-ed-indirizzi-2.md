---
title: Approfondimento chiavi ed indirizzi
subtitle: >-
  Come detto nell’articolo precedente ogni transazione bitcoin richiede una
  chiave pubblica ed una privata, assimilabili relativamente ad un IBAN ed ad un
  PIN.In questo articolo, un po’ tecnico, andremo ad introdurre il concetto di
  chiavi crittografiche. Vedremo come queste chiavi vengono generate, archiviate
  e gestite. Esamineremo anche i vari formati di codifica utilizzati per chiavi
  pubbliche e private.


  In bitcoin viene utilizzata la crittografia a chiave pubblica (o crittografia
  asimmetrica) per creare una coppia di chiavi che controlla di fatto l’accesso
  ai bitcoin in portafoglio, questa coppia di chiavi corrisponde per l’appunto
  con la chiave pubblica e privata. La chiave pubblica è utilizzata per ricevere
  bitcoin invece quella privata per autorizzare le transazioni. La parte
  interessante giunge adesso perché esiste una relazione matematica tra chiave
  pubblica e privata.


  **Principio di generazione chiave privata e pubblica**


  La chiave privata è un numero scelto a caso. Dalla chiave privata, tramite
  l’utilizzo delle curve ellittiche, una funzione di crittografia
  unidirezionale, viene creata la chiave pubblica. Sulla chiave pubblica viene
  utilizzata una funzione di hash crittografica unidirezionale per creare
  l’indirizzo bitcoin.


  Adesso approfondiamo tutti i passaggi passo passo


  * Generazione chiave privata

  * Generazione chiave pubblica, attraverso curva ellittica

  * Generazione dell’indirizzo bitcoin, attraverso la funzione di hash


  **Chiave privata**


  La chiave privata, come già detto, viene utilizzata per creare firme che sono
  necessarie per trasferire bitcoin dimostrando la proprietà dei fondi
  utilizzati nella transazione. Creare una chiave privata non è diverso dallo
  scegliere un numero da 1 e 2^256.


  La chiave privata è un numero, impossibile da prevedere, scelto casualmente
  fra 1 e n − 1, dove n è l’ordine di G (definiremo cosa è G nello specchietto
  successivo). Tale numero deve avere lunghezza 256 bit, per cui viene eseguito
  l’hash SHA-256 avente come output una stringa di lunghezza 256 bit. Se il
  risultato è inferiore a n−1 abbiamo una chiave privata adeguata, altrimenti si
  cerca di nuovo con un altro numero casuale.


  > **curve ellittiche**

  >

  > La curva ellittica usata dal sistema Bitcoin ha forma y2 - x3 + ax + b, che
  varia al variare di a e b. Bitcoin poi pone a = 0 e b = 7, facendo diventare
  così l'equazione y2 = x3+7, chiamata Secp256k1. Tale curva sul piano reale è
  rappresentata nel seguente modo:


  ![](/images/curva-ellettica.png)


  > Il sistema Bitcoin utilizza Secp256k1 definita nel campo (I valori che può
  assumere la coordinata x (e di conseguenza anche la coordinata y) non sono
  tutti gli infiniti valori reali (come succede invece a scuola quando si
  studiano le rette y=ax+b o le parabole y=ax<sup>2</sup>+bx+c) ma sono solo i
  valori che corrispondono a elementi di un insieme molto particolare, detto
  campo) Z<sub>2<sup>256</sup>-2<sup>32</sup>—977</sub> nel quale le coordinate
  x e y sono interi a 256-bit modulo un primo molto grande.

  >

  > Oltre a dei parametri a e b ve ne sono altri quali il modulo (primo) del
  campo, un punto base che si trova sulla curva e l'ordine del punto base, che
  non è scelto casualmente ma è una funzione dipendente dagli altri parametri.
  Bitcoin utilizza dei parametri molto grandi, la sicurezza dell'algoritmo si
  basa su questi valori che risultano difficili da attaccare attraverso un
  attacco a forza bruta. Nel caso del Bitcoin:

  >

  > Modulo (primo):

  >

  > 2<sup>256</sup> – 2<sup>32</sup> – 2<sup>9</sup> – 2<sup>8</sup> –
  2<sup>7</sup> – 2<sup>6</sup> – 2<sup>4</sup> – 1= FFFFFFFF FFFFFFFF FFFFFFFF
  FFFFFFFF FFFFFFFF FFFFFFFF FFFFFFFF FFFFFC2F (in esadecimale)

  >

  > Punto Base G:

  >

  > x = 79BE667E F9DCBBAC 55A06295 CE870B07 029BFCDB 2DCE28D9 59F2815B 16F81798

  >

  >  y = 483ADA77 26A3C465 5DA4FBFC 0E1108A8 FD17B448 A6855419

  > 9C47D08F FB10D4B8

  >

  > Ordine: 

  >

  > FFFFFFFF FFFFFFFF FFFFFFFF FFFFFFFE BAAED- CE6 AF48A03B BFD25E8C D0364141


  Per darvi un’idea della dimensione dello spazio di una chiave bitcoin si pensi
  che essa è approssimativamente di 2^77, gli atomi nell’universo sono stimati
  essere 2^80


  La seguente è una chiave privata mostrata nella sua rappresentazione
  esadecimale (256 cifre mostrate come 64 cifre esadecimali, ognuna da 4 bit):


  1E99423A4ED27608A15A2616A2B0E9E52CED330AC530EDCC32C8FFC6A526AEDD


  **Chiave pubblica e curve ellittiche**


  La chiave pubblica è calcolata partendo dalla chiave privata utilizzando la
  proprietà di moltiplicazione delle curve ellittiche, la quale è un’operazione
  irreversibile (K=k*G dove k è la chiave privata, G è un punto della curva
  ellittica costante chiamato PUNTO DI GENERAZIONE o punto base e K è la chiave
  pubblica risultante).                                        Quindi, partendo
  da una chiave privata sotto forma di un numero generato in modo casuale k, lo
  moltiplichiamo con un punto predeterminato sulla curva denominato punto di
  generazione G per produrre un altro punto in qualche altra parte della curva,
  che corrisponde alla chiave pubblica K.                                 Ne
  risulta che una chiave privata può essere sempre convertita in una chiave
  pubblica, ma una chiave pubblica non può essere riconvertita in una chiave
  privata perché la funzione matematica utilizzata è
  unidirezionale.                                             Quindi prendiamo
  la chiave privata k generata precedentemente e la moltiplichiamo con il punto
  G per trovare la chiave pubblica K:


  K = 1E99423A4ED27608A15A2616A2B0E9E52CED330AC530EDCC32C8FFC6A526AEDD * G


  La Chiave Pubblica K è definita come punto K = (x,y):

  dove,


  x = F028892BAD7ED57D2FB57BF33081D5CFCF6F9ED3D3D7F159C2E2FFF579DC341A


  y = 07CF33DA18BD734C600B96A72BBC4749D5141C90EC8AC328AE52DDFE2E505BDB


  Ricapitolando, la chiave privata è un numero, scelto casualmente fra 1 e n-1,
  dove n è l’ordine di G.                                        Tale numero
  deve avere una lunghezza di 256 bit, per cui viene eseguito l’hash SHA-256 che
  ha come output una stringa di lunghezza
  256bit.                                                           Se il
  risultato è inferiore a n-1 abbiamo una chiave privata adeguata, altrimenti si
  cerca un nuovo numero casuale.                         La chiave pubblica si
  deriva dalla seguente equazione: K=k*G.                         In pratica, la
  creazione della chiave pubblica è suddivisa in una serie di operazioni
  raddoppio e somma di punti, partendo da punto base
  G.                                                                    A
  partire dalla chiave pubblica risulta impossibile dedurre la chiave privata,
  soprattutto se vengono utilizzati dei valori iniziali molto grandi.


  **Indirizzi e chiavi**


  Chiunque voglia ricevere un pagamento, o effettuarne uno, deve per prima cosa
  creare una coppia chiavi pubblica e privata.                     Ogni utente
  che partecipa alla rete crea, grazie ad un client, una chiave privata casuale
  di 256bit.                                         Questa servirà in seguito
  per firmare la transazione e trasferire i bitcoin al nuovo
  proprietario.                                         Da questa chiave si
  genera successivamente la chiave pubblica di 512bit, applicando l’algoritmo
  ECDSA (curve ellittiche).                      Tale chiave viene usata da chi
  riceve il pagamento per verificare che la firma digitale del mittente sia
  autentica.                             La chiave pubblica del mittente
  rappresenta anche il suo indirizzo, che viene condiviso tra gli utenti della
  rete per eseguire le
  transazioni.                                                               La
  chiave che viene creata con ECDSA risulta però molto lunga e ciò può causare
  problemi nella sua trascrizione ed utilizzo.               Per accorciarla e
  renderla facilmente accessibile, si esegue un doppio hash per prima cosa si
  calcola SHA-256 (PubKey), e successivamente si esegue RIPEMD-160
  (SHA-256(PubKey)), infine ogni chiave viene codificata in formato ASCII
  utilizzando l’algoritmo Base58Check che manda in output un indirizzo del tipo:


  1NDpZ2wyFekV ezssSXv2tmQgmxcoHMUJ7u


  costituito da caratteri standard. Gli indirizzi degli utenti bitcoin non sono
  altro che gli hash delle loro chiavi pubbliche.
excerpt: >-
  La chiave privata è un numero scelto a caso. Dalla chiave privata, tramite
  l’utilizzo delle curve ellittiche, una funzione di crittografia
  unidirezionale, viene creata la chiave pubblica. Sulla chiave pubblica viene
  utilizzata una funzione di hash crittografica unidirezionale per creare
  l’indirizzo bitcoin.
img_path: ''
post_button_label: Leggi
date: 2019-11-28T17:00:16.980Z
layout: page
---

