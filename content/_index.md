---
title: Home
sections:
  - type: intro
    content: >-
      Aspettarsi grosse ricompense per piccoli investimenti significa
      incoraggiare un comportamento stupido.
    actions:
      - label: Get Started
        url: /generic
        is_scrolly: false
        is_primary: false
    title: Reflex
    img_path: images/pic01.jpg
    component: intro.html
  - type: spotlight
    content: ''
    actions:
      - label: Details
        url: /generic
        is_scrolly: false
        is_primary: false
    title: Duis torquent
    subtitle: |-
      Rutrum facilisis. Class aptent taciti sociosqu  
      litora torquent et conubia etiam nostra.
    component: spotlight.html
  - type: features
    content: >-
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
    actions:
      - label: Details
        url: /generic
        is_scrolly: false
        is_primary: false
    title: Ipsum malesuada
    subtitle: |-
      Rutrum facilisis. Class aptent taciti sociosqu  
      litora torquent et conubia etiam nostra.
    symbol_display:
      - title: Lorem
        icon: fa-code
      - title: Ipsum
        icon: fa-cog
      - title: Dolor
        icon: fa-diamond
      - title: Feugiat
        icon: fa-camera-retro
      - title: Tempus
        icon: fa-briefcase
    component: features.html
menu:
  main:
    name: Home
    weight: 1
layout: home
---
