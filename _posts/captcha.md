---
title: "I'm NOT a robot! CAPTCHA: cosa sono, a cosa servono e un po' di storia"
date: 2021-01-14
permalink: /posts/2021/01/captcha/

---

> (*leggi l'articolo originale su [Passaporto Futuro](https://www.passaporto-futuro.com/post/i-m-not-a-robot)*)


Durante una semplice navigazione tra le pagine del web, vi sarà sicuramente capitato di imbattervi in una schermata che richiede di confermare che **non siete dei robot**. 
Anche se apparentemente strana, la richiesta di avere questa conferma ha delle radici e delle motivazioni molto chiare, principalmente legate all’azione dei **bot** nelle reti sociali. 


Un bot, infatti, è un programma del tutto automatico in grado di muoversi tra la pagine web (per esempio) con **comportamenti simili a quelli di un essere umano**: inviare messaggi nelle chat, scrivere commenti, ottenere informazioni dalle pagine web e inserire nuove informazioni nelle stesse pagine.

Seppur l’utilizzo dei bot sia generalmente etico e benefico (chatbot, automatizzare tasks, etc.), esistono anche numerosi esempi di bot malevoli (click fraud, attacchi DDoS, spambots, etc.). 
Nel [Annual Bad Bot Report](https://www.imperva.com/blog/bad-bot-report-2020-bad-bots-strike-back/#:~:text=In%202019%2C%20bad%20bot%20traffic,hit%20hardest%20by%20bad%20bots) si stima che la percentuale di traffico internet gestita dai “bad bot” sia stata del 24.1% contro quella del 13.1% dei “good bot”, nel 2019.

Il possibile comportamento malevolo di questi programmi è stato la causa dell’invenzione del **CAPTCHA** (**C**ompletely **A**utomated **P**ublic **T**uring test to tell **C**omputers and **H**umans **A**part), la tecnologia in grado di distinguere un essere umano da un computer, che ha permesso di “limitare” l’accesso ai bot ad alcune pagine in cui è richiesta maggiore sicurezza (login, acquisto di prodotti, chat e forum, etc.).


La nascita di questo sistema è ricondotta a Luis von Ahn in una [pubblicazione](https://link.springer.com/chapter/10.1007%2F3-540-39200-9_18) del 2003 anche se, alcuni anni prima (1997) il team di R&D di AltaVista (un motore di ricerca) aveva implementato qualcosa di simile per evitare il riconoscimento delle immagini da parte di scanner ottici.

---

### Test di Turing

Nell’acronimo “**CAPTCHA**” appare il termine “turing test”. Di cosa si tratta?

Nel 1950, il matematico Alan Turing (noto per la [Macchina di Turing](https://it.wikipedia.org/wiki/Macchina_di_Turing) e per essere riuscito a decifrare i messaggi crittografati dalla macchina [Enigma](https://it.wikipedia.org/wiki/Enigma_(crittografia)) utilizzata dei Nazisti durante la Seconda Guerra Mondiale) ideò il **Turing test**.



> *“I propose to consider the question, ‘Can machines think?’”*

Questa è la domanda utilizzata da Turing nell’apertura della sua [pubblicazione](https://academic.oup.com/mind/article-pdf/LIX/236/433/9866119/433.pdf) in cui descrive il “gioco dell’imitazione”.


L’idea è quella di capire se un computer sia in grado di **imitare** il comportamento di un essere umano. Il gioco, come descritto originariamente da Turing, è composto da tre “giocatori”: un uomo (A), una donna (B) e un interrogatore (C) che può essere di entrambi i sessi. 

L’interrogatore sta in una stanza separata dagli altri due e pone domande ad A e B in modo tale da generare una decisione (A è uomo e B è donna, oppure, A è donna e B è uomo) in base alle risposte ricevute (le risposte vengono scritte a macchina per evitare che la voce o la calligrafia possano influenzare la decisione).

Turing propone poi di scambiare l’uomo (A) con un computer e chiede: 

> *“Will the interrogator decide wrongly as often when the game is played like this as he does when the game is played between a man and a woman?”*

Ovvero: **l’interrogatore è in grado di distinguere chi è la macchina e chi è l’essere umano?**

Ricapitolando, senza procedere oltre in questa discussione, il test di Turing permette di distinguere un computer (un bot) da un essere umano in base al loro comportamento.

Nel caso specifico del CAPTCHA, si parla di **reverse Turing test**, in quanto l'interrogatore non è un essere umano ma esso stesso un computer.

---

### Versioni di CAPTCHA

Negli anni si sono susseguite varie versioni del CAPTCHA. 


#### Versione originale (“smwm”)

La versione originale (chiamata anche “**smwm**”) rappresenta il tentativo del gruppo di AltaVista di impedire agli scanner ottici ([OCR](https://it.wikipedia.org/wiki/Riconoscimento_ottico_dei_caratteri)) di riconoscere il testo in un immagine. Nel manuale dello scanner che stavano utilizzando in quel periodo erano presenti alcune raccomandazioni per migliorare i risultati dello scanner:
* caratteri definiti e lineari
* stesso font di carattere tra le lettere (o simili)
* sfondo omogeneo e in contrasto con il testo
Con l’obiettivo di rendere il riconoscimento il più difficile possibile, il gruppo decise di applicare queste raccomandazioni al contrario, creando delle immagini che avessero **caratteri confusi e distorti**, **font diverso** e **sfondo non omogeneo**.

Il CAPTCHA che si basa su questa versione mostra all’utente l’immagine di un testo con le caratteristiche sopra descritte e richiede di inserire il contenuto testuale in una casella posta sotto all’immagine.



Prima che il Machine Learning e l’Intelligenza Artificiale permettessero l’implementazione di buoni sistemi di riconoscimento del testo, questo metodo era piuttosto consolidato e sicuro per evitare che un bot riuscisse ad entrare in una pagina web.

Nonostante alcuni miglioramenti siano stati apportati a questa tecnica (come l’aggiunta di **elementi di disturbo**), programmi basati su metodi di Machine Learning sono comunque in grado di aggirare questo ostacolo.

Oggigiorno, infatti, il riconoscimento del testo da parte di un computer è un task relativamente semplice e, per questo, il CAPTCHA ha dovuto evolversi in forme più complesse.


#### Versioni avanzate

Altre versioni, che iniziano comunque a risentire dello stesso problema della versione “smwm”, ovvero del così detto “**machine learning-based attack**”, sono quelle che richiedono di:
* risolvere un quiz matematico
* individuare tutte le immagini che contengono semafori, auto o camion (per esempio)
* identificare una specifica lettere all’interno di un testo distorto
* accedere utilizzando l’account Google o Facebook (si presuppone che un bot non conosca username e password dell’utente)



Tutte le tecniche qui elencate (ne esistono molte altre) si basano su un’interazione con l’utente, il che, spesso, potrebbe risultare noiosa e comportare un eventuale abbandono della pagina da parte dell’utente stesso.


#### Versione Honeypot

Per ovviare al problema della continua interazione con l’utente una soluzione interessante è quella dell’**Honeypot**.

Questa tecnica consiste nell’inserire all’interno della pagina web numerosi campi nascosti alla vista dell’essere umano ma visibili ai bot che per come sono generalmente costruiti, tendono a riempire tutti i form che “vedono” all’interno del codice di una pagina web. 

Chiunque, anche senza basi di programmazione, che si appresta a implementare una pagina web, è in grado di inserire dei “form” all’interno della pagina stessa che non sono visibili all’utente ma che, in quanto scritti nel codice sorgente, sono visibili ai bot che tentano di effettuare l’accesso.

L’idea è che, nel momento in cui un form nascosto viene riempito, questo è un chiaro segnale della presenza di un bot.

Nonostante l’idea sia interessante e priva di interazione con l’utente, anche in questo caso esistono bot in grado di aggirare questa limitazione.


#### Versione reCAPTCHA

La versione più innovativa e moderna del CAPTCHA è quella chiamata **reCAPTCHA**, implementata da Luis von Ahn a partire dal 2007 e successivamente acquistata da Google nel 2009.



Dietro la creazione della startup capitanata da von Ahn, c’è una [storia](https://techcrunch.com/2007/09/16/recaptcha-using-captchas-to-digitize-books/?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAH2Vxhv1lazhtg2VaX-l6nZQ9tUlHY_SrP7AtWzBg_9jupI4yFO_kOD6kbHz7tLeC0loEBWQQOMzA883ISKwhJaySmQ3BxIEfVla7dGpqYq3bJC-I0TFZROLeMpyCIQg2FypB-RaoYhAmv304KDskkQKyfDng23-gNGGizmFlj3s) molto interessante: lo scopo iniziale era quello di utilizzare i CAPTCHA per aiutare la digitalizzazione di libri antichi. I sistemi classici (OCR) avevano difficoltà ad identificare le lettere sbiadite di alcune parole: l’idea è stata, quindi, quella di far riconoscere queste parole dagli utenti utilizzandole come testo nei CAPTCHA a loro forniti. Un classico esempio di **gioco con uno scopo** che ha permesso di riconoscere e digitalizzare 4 milioni di parole al giorno (nel 2008) richiedendo uno sforzo umano che sarebbe stato altrimenti “sprecato”.

La tecnologia che sta alla base della più recente versione del reCAPTCHA ([reCAPTCHA v3](https://developers.google.com/recaptcha/docs/v3)) di Google, analizza ed utilizza il **comportamento passato** di un utente per capire se esso sia un essere umano oppure un bot. Questa analisi è facilmente permessa dalla grande quantità di dati che Google possiede di ognuno di noi: movimenti del mouse nello schermo, velocità di digitazione e compilazione di un form, click, scroll delle pagine e così via.

È applicando le tecniche di Machine Learning e Intelligenza Artificiale più avanzate che Google e il reCAPTCHA v3 riescono ad associare ad ogni utente (umano o bot) un **punteggio** che rappresenta quanto il suo comportamento sia stato simile a quello generalmente adottato da un umano. E questo viene fatto in maniera del tutto invisibile all’occhio dell’utente: nella maggior parte dei casi, durante la navigazione in una pagina web, il reCAPCTHA lavora in background analizzando il comportamento dell’utente e stabilendo il relativo punteggio.

In alcuni casi, qualora il punteggio sia troppo vicino alla soglia che discrimina tra macchina e umano, può comunque esserci la classica richiesta di riconoscimento di un testo o di un immagine.

Questa soluzione unisce **ottimi risultati** con una **pressoché nulla interazione** con l’utente.

---

### Conclusioni

Come per molte moderne tecnologie, anche per i CAPTCHA la quantità di dati a disposizione risulta essere una discriminante importante per riconoscere e distinguere tra un essere umano e un bot. 

Se da un lato si fanno voce molte polemiche riguardanti la **privacy dei dati** e l’utilizzo che le grandi multinazionali come Google ne fanno, dall’altro risulta evidente che questi stessi dati sono spesso fondamentali per risolvere altri tipi di problemi e permettere avanzamenti tecnologici.


Nei prossimi anni saranno sicuramente implementati altri miglioramenti di queste tecniche con lo scopo di limitare attacchi di bot sempre più avanzati e di ridurre al minimo l’interazione con l’utente per garantire una più piacevole navigazione ed **evitare di dover chiedere se siamo dei robot**.
