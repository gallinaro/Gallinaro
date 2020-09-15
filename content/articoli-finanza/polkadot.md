---
title: Polkadot
subtitle: >-
  **Introduzione**


  Polkadot è una blockchain innovativa che punta a superare quelli che sono i 2 principali limiti delle piattaforme attualmente disponibili, cioé scalabilità e iper-specializzazione. Per superare il limite della scalabilità, Polkadot utilizza la tecnica dello sharding, ovvero divide la blockchain in tanti frammenti che vengono coordinati da una blockchain centrale con il compito di mettere assieme tutti i pezzi e di conseguenza va a smistare la gravosità del compito in diverse parti, aumentando in maniera esponenziale il numero di operazione che può compiere. Per quanto riguarda l’iper-specializzazione, Polkadot consente l’interoperabilità, più blockchain specializzate possano interagire e cooperare per creare un ecosistema estremamente vasto.


  ![](/images/polkadot-ecositemaa.png)


  **Struttura ed architettura**


  Polkadot ha una struttura ed architettura modulare, è composta da diverse componenti che si ripetono e che lavorano sinergicamente tra loro.


  **Relay-chain**


  Il modulo più importante di tutti è la Relay chain, il cuore di Polkadot: è responsabile della sicurezza condivisa, del consenso e dell’interoperabilità cross-chain della rete.


  ![](/images/arelay-chain-polkadot.png)


  Sulla relay chain circola il token proprietario di Polkadot, DOT. Il token DOT serve innanzitutto per la governance, gli holder del token sono incentivati a votare e/o proporre nuove modifiche per far evolvere l’ecosistema. Questo sistema permette a Polkadot di eseguire l’aggiornamento senza hard fork per integrare nuove funzionalità o correggere bug (es. diluizione della supply x 100). Il sistema quindi può aggiornarsi non appena saranno disponibili tecnologie migliori. Altro compito della relay chain è garantire la sicurezza, questo grazie ad un algoritmo di consenso proprietario (una sorta di proof of stake). Infine l’ultimo compito è quello di coordinare le attività che permettono l’interoperabilità delle diverse chain, che significa sia coordinare le blockchain native di polkadot (parachain) o esterne come quelle di Ethereum.


  **Parachains**


  E’ la componente specifica del sistema Polkadot, sono delle vere e proprie blockchain sviluppate all’interno del sistema polkadot ed ognuna di esse ha il suo token. E’una blockchain a sé stante ed è deputata a fare qualcosa di specifico e particolare.


  ![](/images/apara-chian-polkadot.png)


  Ogni sviluppatore può creare la propria parachain utilizzando il framework Substrate ed essa poi si integrerà con le altre e alla blockchain esterne grazie alla relay chain. Per creare nuove parachain occorre vincolare dei Dot con l’operazione denominata Bonding, questo al fine di evitare la creazione di eccessive parachain superflue (l’operazione rende costoso avere una parachain). Una volta che si decide di ritirare una parachain si svincolano i token DOT


  **Bridges**


  Infine abbiamo i bridges, che consentono alla parachain di connettersi e comunicare con reti esterne come Ethereum o Bitcoin e permettono quindi di collegare il mondo Polkadot con le blockchain esterne, anch’esse sono delle blockchain con un token proprio (es Darwinia )


  ![](/images/abridges-polkadot.png)


  **Consenso**


  Per mantenere sicuro il sisma ci sono 4 ruoli che sinergicamente partecipano a questo scopo: Nominator, Validator, Collator e Fishermen


  **Nominators**


  Sono i nodi deputati a nominare i validatori. Il potere di nomina viene acquisito facendo staking del token Dot


  ![](/images/anominators-polkadot.png)


  **Validators**


  Lo scopo dei validators è quello di andare a validare le transazioni ed i blocchi della blockchain. Anche i validatori dovranno essere token holder e dovranno fare staking in misura maggiore dei nominators.


  ![](/images/avalidators-polkadot.png)


  **Collators**


  Rappresentano coloro che devono recuperare tutte le transazioni dei vari shard, le elaborano e producono delle prove (proofs):queste vengono passate ai validators per la validazione stessa.


  ![](/images/acollators-polkadot.png)


  **Fishermen**


  Servono a monitorare la rete e a segnalare il cattivo comportamento ai validatori: la penitenza per il comportamento scorretto può arrivare anche allo slashing, cioé alla perdita dei DOT che vengono vincolati al noto affinchè questo possa compiere il suo dovere. Questo ruolo può essere svolto sia dai full node delle parachain che dai collators


  ![](/images/afishermen-polkadot.png)
excerpt: Polkadot è una blockchain innovativa che punta a superare quelli che
  sono i due principali limiti delle piattaforme attualmente disponibili, quindi
  scalabilità e della iper-specializzazione.
img_path: ''
post_button_label: Leggi
date: 2020-09-11T17:18:40.153Z
layout: page
---
