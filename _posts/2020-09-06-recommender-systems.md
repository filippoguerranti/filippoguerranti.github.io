---
title: 'Recommender Systems'
date: 2020-09-06
permalink: /posts/2020/09/recommender-systems/
tags:
  - cool posts
  - category1
  - category2
---

Il successo ottenuto negli ultimi anni da aziende come Netflix, Amazon e Youtube (solo per citarne alcuni) può essere in parte ricondotto all’utilizzo estenuante dei sistemi di raccomandazione (SR nel seguito): algoritmi in grado di suggerire ad ogni utente un prodotto che sia il più rilevante possibile per l’utente stesso. 

La sezione “suggerimenti per te” di Netflix o quella “consigliati in base ai tuoi interessi” di Amazon sono ottimi esempi di SR. Lì vengono proposti film o prodotti significativo per l’utente in base al suo comportamento passato o alle sue caratteristiche.

Tecnicamente parlando esistono due tipi di SR: il metodo del filtro collaborativo (collaborative filtering) e quello basato sui contenuti (content based).

Il collaborative filtering si basa sulle interazioni passate tra utenti e prodotti con lo scopo di produrre nuovi suggerimenti. Si può considerare “interazione” la votazione di un prodotto, o il semplice like/dislike utilizzato da Netflix.
Il vantaggio di questo metodo è che non è necessaria alcuna informazione riguardo agli utenti e ai prodotti ma risente di un problema chiamato “cold start”: per un nuovo prodotto o per un nuovo utente non esiste una storia passata e risulta impossibile creare nuovi suggerimenti.

I content based, oltre ad utilizzare le interazioni utenti/prodotti utilizzano anche le informazioni riguardo ad essi (content). Il SR utilizzato da Netflix per suggerire un film potrebbe tenere in considerazione la categoria, gli attori principali, la durata e altre caratteristiche del film stesso oltre all’età e al sesso dell’utente. 
L’idea dei metodi content based è quella di creare un modello che descriva il fatto che un giovane tende a valutare meglio un determinato genere di film, un adulto tende a valutarne meglio un altro, e così via.

Per capire quanto un SR possa essere economicamente importante per un'azienda, basta pensare al premio di 1M di dollari indetto da Netflix per chiunque riuscisse a migliorare del 10% la precisione del SR utilizzato fino a quel momento. 

Quanto ritieni attinenti i suggerimenti che vedi su internet?

------
