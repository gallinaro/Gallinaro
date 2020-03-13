---
title: Home page
sections:
  - actions: []
    component: intro.html
    content: >-
      Aspettarsi grosse ricompense per piccoli investimenti significa
      incoraggiare un comportamento stupido.
    img_path: /images/img_6khgjhgk285.jpg
    title: Gallinaro
    type: intro
  - type: features
    title: Categorie
    component: features.html
    actions:
      - is_scrolly: false
        is_primary: true
        label: Bitcoin
        url: /bitcoin-post
      - is_scrolly: false
        is_primary: false
        label: Finanza
        url: /finanza-post
  - actions: []
    component: spotlight.html
    content: ''
    subtitle: ''
    title: Ultimi Articoli
    type: spotlight
  - component: features.html
    content: "<script>\r\n\n   if (typeof(stockdio_events) == \"undefined\") {\r\n\n\\    stockdio_events = true;\r\n\n\\    var stockdio_eventMethod = window.addEventListener ? \"addEventListener\" : \"attachEvent\";\r\n\n\\    var stockdio_eventer = window\\[stockdio_eventMethod];\r\n\n\\    var stockdio_messageEvent = stockdio_eventMethod == \"attachEvent\" ? \"onmessage\" : \"message\";\r\n\n\\    stockdio_eventer(stockdio_messageEvent, function (e) {\r\n\n\\    if (typeof(e.data) != \"undefined\" && typeof(e.data.method) != \"undefined\") {\r\n\n\\    eval(e.data.method);\r\n\n\\    }\r\n\n\\    },false);\r\n\n   }\r\n\n</script>\r\n\n<iframe id='st_2a3cf2a3a3404f71893fc6063891dd7a' frameBorder='0' scrolling='no' width='100%' height='100%' src='https://api.stockdio.com/visualization/financial/charts/v1/Ticker?app-key=796FC8FA75684B0990FADB79432CAC11&stockExchange=CRYPTO&symbols=BTC;ETH;XRP;BCH;LTC;&culture=Italian-Italy&motif=Material&palette=Aurora&layoutType=14&googleFont=true&backgroundColor=f7f7f7&labelsColor=2b2d30&onload=st_2a3cf2a3a3404f71893fc6063891dd7a'></iframe>"
    title: Andamenti
    type: features
menu:
  main:
    name: Home
    weight: 1
layout: home
---
