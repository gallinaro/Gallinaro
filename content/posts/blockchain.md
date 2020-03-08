---
title: Blockchain
subtitle: >-
  Il paradigma tradizionale delle transazioni prevede che nello scambio di asset
  tra due utenti si faccia riferimento ad un’autorità centrale, la trusted third
  party
  (TTP).                                                                                  
  Questo ente ha il compito di registrare lo storico delle transazioni degli
  utenti, in modo da poter ricostruire in ogni momento lo stato del sistema.


  > Esempio

  >

  > Pagamento tramite carta di credito: 2 utenti devono passare attraverso la
  banca, questa da un lato garantisce che l'utente che cede denaro abbia la
  disponibilità economica per farlo e dall'altro che la transazione avvenga con
  successo.


  La presenza di questo ente centrale è necessaria per garantire il corretto
  funzionamento del servizio.

   **Storia Blockchain e Bitcoin**

  Non si può non accennare a Bitcoin quando si vuole introdurre l’argomento
  blockchain.                          Nel 2008 Satoshi Nakamoto (pseudonimo)
  propone un’alternativa alla centralizzazione discussa prima, progettando la
  prima blockchain, in grado di garantire transazioni Bitcoin senza la necessità
  della garanzia di un ente centrale.


  > Bisogna specificare che il termine Bitcoin indica sia la valuta che viene
  scambiata, sia il protocollo che gestisce il sistema, inoltre è opportuno
  sottolineare che il protocollo Bitcoin definisce una blockchain, non la
  blockchain in generale


  Il Bitcoin è stato inventato nel 2008 con la pubblicazione di un paper
  scientifico intitolato “Bitcoin:A peer-to-peer electronic cash system” da
  Nakamoto.                                                                                       
  Bitcoin è un contante elettronico completamente decentralizzato che non
  dipende da nessuna autorità centrale per l’emissione, la liquidazione e la
  validazione delle
  transazioni.                                                                 
  Combinando alcune tecnologie già affermate (crittografia e comunicazione tra
  nodi), Nakamoto presenta la prima rete di scambio P2P completamente
  decentralizzata che permette agli utenti di scambiarsi direttamente del denaro
  senza passare per un ente
  centrale.                                                                                                                       
  Rispetto alle tradizionali transazioni la tecnologia blockchain prevede che
  tutti i nodi che fanno parte della rete possiedano una copia del registro
  delle transazioni, rendendolo così accessibile a
  tutti.                                                    Inoltre, il
  protocollo fa in modo che le copie del registro in mano a differenti nodi
  siano coerenti tra loro, così da non poter ingannare il
  sistema.                                                                                                                              
  Il network bitcoin è basato sull’implementazione di riferimento pubblicata da
  Nakamoto, essendo esso open source da quel momento in poi è stato visto e
  modificato da molti altri programmatori, la conseguenza è stata la nascita di
  migliaia di criptovalute alternative a
  Bitcoin.                                                Inoltre, ci si è resi
  conto che soffermarsi alle criptovalute è estremamente riduttivo, in quanto la
  tecnologia blockchain permette di decentralizzare le transazioni di qualsiasi
  asset digitale.                                                 Questa
  tecnologia ha infatti la capacità di sostituirsi a qualsiasi ente che
  controlli in modo centralizzato una rete o un sistema.


  **Introduzione alla Blockchain**


  Un prima definizione di blockchain la descrive come un archivio permanente che
  memorizza e gestisce transazioni; queste vengono immagazzinate in blocchi solo
  dopo che la rete stessa ha approvato e verificato la correttezza delle
  informazioni, di conseguenza ciascun blocco è contemporaneamente archivio e
  controllore di tutte le
  transazioni.                                                                                                                                
  Il fatto che tutti i partecipanti siano collegati tra loro permette la
  tracciabilità e garantisce l’immutabilità delle transazioni avvenute grazie
  anche all’utilizzo della
  crittografia.                                                                      
  Una secondo interpretazione della blockchain è quella di registro pubblico DLT
  (Distributed Ledger Technology), ovvero Libro Mastro distribuito in quanto non
  esiste il concetto di sistema centralizzato, bensì una nuova logica in cui
  tutti i membri sono di pari livello e in cui si instaura un rapporto di
  fiducia tra essi.              Si tratta quindi di una rete peer-to-peer in
  cui vengono registrate le transazioni e i dati di chi le
  esegue.                                                                                  
  Quello che è innovativo nella blockchain è il concetto di libro mastro
  distribuito e condiviso, ovvero un registro immutabile contenente tutte le
  transazioni avvenute in un certo network e a cui possono accedere, in modo
  rapido, tutti i partecipanti del network stesso, grazie al fatto che il
  database non si trova fisicamente su un solo server, ma su tutti i computer
  partecipanti alla
  rete.                                                               Sul lato
  teorico quindi ogni nodo dovrebbe salvare una copia del registro sul proprio
  dispositivo, tuttavia sul lato pratico questa attività richiede un enorme
  spazio di archiviazione che i dispositivi comuni non
  hanno.                                                                                                                                                                    
  Nella pratica dunque abbiamo 2 livelli di nodi: full e
  light                                                                                                                     


  * I nodi full rappresentano la struttura che sostiene la rete intera, solo tra
  questi viene distribuito il registro delle transazioni.

  * I nodi  light invece rappresentano un livello gerarchico inferiore, in grado
  soltanto di consultare il registro e di comunicare con i nodi full.


  Ogni nodo a prescindere dal proprio livello può inoltre ricoprire 2 ruoli
  all'interno della rete: nodo Wallet o nodo miner


  * Il nodo wallet, quelli che gestiscono una serie di indirizzi che
  identificano il nodo e l'utente e che permettono di inviare e ricevere
  transazioni.

  * Il nodo miner, sono quei nodi che supportano direttamente il funzionamento
  della blockchain effettuando operazioni di verifica e conferma delle
  transazioni e di stesura del registro stesso.


  ![](/images/levels-of-distribution.png)


  Le informazioni della blockchain vengono immagazzinate in blocchi collegati
  tra loro a creare una catena, per cui al crescere del numero delle
  transazioni, aumenta anche il volume della
  blockchain.                                                                                             
  Ogni blocco associa alla transazioni valide una marca che contiene il proprio
  codice hash e quello del blocco precedente.


  > Funzioni di hash

  >

  > è un algoritmo che elabora un input di lunghezza variabile e lo trasforma in
  un output di lunghezza fissa chiamato hash


  Questo impedisce che i blocchi vengano alterati o che ne venga inserito uno
  tra due già
  collegati.                                                                                      
  Grazie alla grande accessibilità di questa tecnologia, sono nati molti tipi di
  blockchain che variano tra loro in quanto offrono soluzioni diverse ai comuni
  problemi queli la decentralizzazione, la scalabilità e la
  sicurezza.                                                                                                                                                                          
  Le blockchain non possono mai eccellere in questi 3 campi contemporaneamente,
  ma devono scendere a compromessi.


  > Esempio

  >

  >  Bitcoin rinuncia alla scalabilità in cambio di decentralizzazione e
  sicurezza.


  (in aggiornamento...)
excerpt: >-
  Un prima definizione di blockchain la descrive come un archivio permanente che
  memorizza e gestisce transazioni; queste vengono immagazzinate in blocchi solo
  dopo che la rete stessa ha approvato e verificato la correttezza delle
  informazioni, di conseguenza ciascun blocco è contemporaneamente archivio e
  controllore di tutte le transazioni.
img_path: ''
post_button_label: Leggi
date: 2019-07-30T22:00:00.000Z
layout: page
---

