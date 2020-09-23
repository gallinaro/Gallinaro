---
title: Bitcoin post
sections:
- actions:
      - is_scrolly: false
        is_primary: true
        label: Home
        url: /_index
  - type: spotlight
    content: ''
    actions: []
    title: Articoli bitcoin
    subtitle: ''
    component: bitcoin-spotlight.html
  - type: features
    title: Andamenti 
    component: features.html
    subtitle: >-
      <script>

         if (typeof(stockdio_events) == "undefined") {

      \    stockdio_events = true;


      \    var stockdio_eventMethod = window.addEventListener ?
      "addEventListener" : "attachEvent";


      \    var stockdio_eventer = window\[stockdio_eventMethod];


      \    var stockdio_messageEvent = stockdio_eventMethod == "attachEvent" ?
      "onmessage" : "message";


      \    stockdio_eventer(stockdio_messageEvent, function (e) {


      \    if (typeof(e.data) != "undefined" && typeof(e.data.method) !=
      "undefined") {


      \    eval(e.data.method);


      \    }


      \    },false);

         }

      </script>


      <iframe id='st_2a3cf2a3a3404f71893fc6063891dd7a' frameBorder='0'
      scrolling='no' width='100%' height='100%'
      src='https://api.stockdio.com/visualization/financial/charts/v1/Ticker?app-key=796FC8FA75684B0990FADB79432CAC11&stockExchange=CRYPTO&symbols=BTC;ETH;XRP;BCH;LTC;&culture=Italian-Italy&motif=Material&palette=Aurora&layoutType=14&googleFont=true&backgroundColor=f7f7f7&labelsColor=2b2d30&onload=st_2a3cf2a3a3404f71893fc6063891dd7a'></iframe>
menu:
  main:
    name: Bitcoin
    weight: 
layout: home
---
