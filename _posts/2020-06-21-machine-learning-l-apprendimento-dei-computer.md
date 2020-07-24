---
title: 'Machine Learning: come apprendono i computer'
date: 2020-06-21
permalink: /posts/2020/06/machine-learning-l-apprendimento-dei-computer/

---

Negli ultimi anni i termini Machine Learning e Intelligenza Artificiale sono stati spesso utilizzati in molti contesti della nostra società: se ne sente parlare in ambiti informatico, economico, sanitario e farmacologico, oltre che in molti altri.
Seppure i due termini siano molto correlati, è bene capire che non indicano affatto lo stesso concetto.

L’Intelligenza Artificiale è la disciplina che studia come rendere una macchina (un computer) in grado di compiere task “intelligenti”. Si definisce, perciò, una “Intelligenza Artificiale” qualunque dispositivo che sappia imitare in qualche modo il comportamento umano: un esempio è la capacità di riconoscere due immagini, una di un gatto e una di un cane, e classificarle come “gatto” e come “cane”, rispettivamente.

Il Machine Learning, tradotto generalmente in italiano come “apprendimento automatico”, è una branca del più ampio concetto di Intelligenza Artificiale e rappresenta la capacità di un computer di apprendere in modo “relativamente” autonomo.

Facciamo un parallelismo per capire meglio. Gli esseri umani sono dotati di una intelligenza che li rende capaci di muoversi, di parlare e di imparare (oltre a tante altre cose). Esattamente come un essere umano, anche un computer può essere dotato di un’intelligenza, ma in questo caso “artificiale”: questo tipo di intelligenza permette alla macchina di muoversi (robot), di parlare (assistenti vocali come Siri o Alexa) e di imparare.

È nell’apprendimento che il Machine Learning entra in gioco ed è per questo motivo che rappresenta solamente un sottoinsieme del ben più ampio concetto di Intelligenza Artificiale, il quale comprende anche tutte le altre applicazioni di una comune intelligenza.

*Ma come fa un computer ad apprendere e, soprattutto, cosa deve apprendere?*


Pensiamo per un attimo alla programmazione tradizionale come ad un processo manuale.

Ogni algoritmo che un programmatore si presta ad implementare in modo manuale, richiede una certa quantità di dati in input, ovvero in ingresso all’algoritmo stesso. Questi dati vengono processati dal programma scritto esplicitamente dal programmatore e, al termine dell’esecuzione, si potranno ottenere alcuni dati di output desiderati. La chiave, in questo processo, sta proprio nella scrittura della logica dell’algoritmo da parte di una persona: è il programmatore che deve capire come strutturare l’algoritmo in modo che dai dati in ingresso si ottengano i dati di uscita desiderati.

Nel Machine Learning l’implementazione della logica dell’algoritmo avviene in modo automatico. Il ruolo del programmatore sta nel scegliere la giusta “architettura” dell’algoritmo ma è il computer, tramite la comparazione tra i dati in ingresso e i dati di uscita desiderati (chiamati “target” o “label”), che apprende in modo “autonomo” i parametri interni all’algoritmo.

L’apprendimento autonomo dei parametri interni dell’algoritmo può essere pensato come alla calibrazione che un fotografo effettua alla propria macchina fotografica per ottenere la foto migliore in termini di luminosità, colori e nitidezza. Allo stesso modo un computer calibra determinati parametri del proprio algoritmo interno (la cui struttura è stata scelta da un programmatore) con il fine di ottenere il miglior risultato possibile in termini di una certa funzione, chiamata “funzione di costo”.

È chiaro, adesso, quale sia la differenza tra ML e IA e, in particolare, cosa vuol dire “apprendimento automatico”.

In questo articolo parleremo dei due principali metodi di apprendimento:
* Supervised Learning o Apprendimento Supervisionato;
* Unsupervised Learning o Apprendimento Non Supervisionato.

In entrambi i casi l’ingrediente fondamentali sono i dati ed è proprio grazie alla grande quantità di dati e alla sviluppata capacità di calcolo di cui disponiamo in questi anni che l’Intelligenza Artificiale e il Machine Learning hanno avuto grande successo.


**Apprendimento Supervisionato.**

La maggior parte dei metodi pratici di ML utilizzano l’apprendimento supervisionato. In questo contesto si prevede che ognuno degli elementi che definiscono l'insieme dei dati in input, quelli di cui il computer dispone, sia dotato di un’etichetta (in gergo tecnico “label”) che definisce l’output desiderato da quel particolare dato in ingresso. Possiamo considerare il label come una sorta di “insegnante” (o “supervisore”, da qui il termine “supervisionato”) per l’algoritmo e, di solito, il processo di associazione dell’etichetta ad ogni singolo dato di input viene svolto da un essere umano.

Chiamiamo l’insieme dei dati di input “training set” ovvero l’insieme dei dati su cui il computer si allenerà. Data la coppia (dato, etichetta), la macchina cercherà di calibrare i propri parametri interni con il fine di associare ad ogni dato di ingresso l’esatto output desiderato.
Quando la macchina avrà concluso il proprio allenamento, dunque avrà elaborato tutto il training set, sarà possibile utilizzarla sui dati “veri”, quelli di cui non sappiamo l’output desiderato ma di cui vogliamo conoscerlo.

Facciamo un esempio pratico per capire meglio cosa questo voglia dire. In particolare descriviamo quello che viene chiamato “problema di classificazione di immagini”:

* supponiamo di avere una grande raccolta di immagini (di cani e gatti per esempio) e supponiamo che per ognuna di queste immagini sia fornita l'opportuna etichetta (gatto o cane). Questo è il nostro Training Set;
* forniamo il training set al computer, ovvero facciamo “vedere” ogni singola immagine al computer e gli permettiamo di conoscere il label associato. Il computer assocerà tutte le immagini raffiguranti un gatto all’output “gatto” e tutte quelle raffiguranti un cane all’output “cane”. 


Questa è la fase di Training in cui il computer viene allenato a riconoscere le immagini del set di immagini in ingresso modificando i propri parametri interni;
* quando la fase di training è conclusa e i parametri interni sono stati opportunamente settati così da riconoscere le immagini di cani e di gatti, la macchina sarà in grado di essere applicata a immagini prive di etichette e di sfruttare la conoscenza appena acquisita per classificarle correttamente.

L’apprendimento, quindi, si dice supervisionato quando i dati su cui la macchina si allena sono dotati di un’etichetta che ne stabilisce la classe di appartenenza (nei problemi di classificazione) o il generico output desiderato (nei problemi di regressione, per esempio) e la macchina, completato l’allenamento, sarà in grado di creare una relazione generale tra dati in ingresso e dati in uscita.


**Apprendimento Non Supervisionato.**

Mentre nel contesto supervisionato ad ogni dato era associato il corrispondente output, nel caso dell’apprendimento non supervisionato il label non è più presente. Ogni dato viene fornito direttamente alla macchina e a questa verrà richiesto di trovare una o più relazioni tra i dati stessi. In questo contesto l’insegnante sparisce e lascia in mano al computer l’intero processo di apprendimento: quello che ci aspettiamo è che venga “scoperta” una certa struttura apparentemente nascosta tra i dati.

Come al solito, consideriamo un esempio per comprendere meglio questo procedimento di apprendimento: il “clustering di documenti” (la parola “clustering” può essere tradotta come “raggruppamento”). Supponiamo di avere una grande raccolta di documenti di testo e immaginiamo ogni documento come un insieme di parole. Se eliminiamo da questo insieme di parole quelle che offrono poche informazioni (come ad esempio le congiunzioni e gli articoli), quello che ci rimane è l’insieme di parole significative per ogni documento.

Ottenuti gli insiemi di parole significative per tutti i documenti, l’algoritmo ne calcola la “similarità”, ovvero calcola quanto due documenti sono simili tra di loro.
Esistono varie tecniche, poi, che permettono di raggruppare articoli simili facendo affidamento su questa misura di similarità per separarli da quelli diversi. Con questo criterio si creeranno, quindi, diversi gruppi ognuno contenente i documenti che trattano argomenti affini.

Algoritmi come quello appena mostrato sono alla base dei motori di ricerca come Google, che mostrano tutte le pagine web contenenti le parole digitate nella barra di ricerca, e degli e-commerce come Amazon, i quali a seguito di un acquisto fatto, suggeriscono al cliente prodotti simili o prodotti comprati da altri utenti che hanno precedentemente fatto acquisti simili.

L’apprendimento non supervisionato ha come principale scopo, dunque, quello di trovare una certa struttura dei dati che gli vengono forniti in ingresso raggruppandoli o associandoli con determinate regole geometriche o probabilistiche.



Supervisionato o non supervisionato, il Machine Learning riscontra grande utilità in molte applicazioni. È utilizzato per:
* far apprendere a specifici software quale possa essere l’andamento di una particolare azione in borsa basandosi sui dati storici precedenti;
* “insegnare” ad un’applicazione per smartphone a classificare un neo della pelle come maligni o benigni tramite una foto aiutando i medici nelle loro diagnosi;
* allenare gli assistenti vocali, come Siri o Alexa, a riconoscere le parole che vengono loro pronunciate;
* calibrare i parametri interni dei complessi algoritmi utilizzati nell’implementazione delle auto a guida autonoma.

Qualunque sia l’applicazione che se ne faccia, il Machine Learning ha permesso di fare grandi passi in avanti in moltissimi ambiti dell’Intelligenza Artificiale grazie alla capacità di apprendere da una grande mole di dati (i cosiddetti Big Data) in tempi relativamente brevi. Quello che prima richiedeva molto tempo per essere elaborato, adesso viene risolto in pochi secondi e si prevede che le potenzialità mostrate finora da questa tecnologia possano essere solo la punta di un iceberg piuttosto grande.

Scacciato l’alone di magia che spesso aleggia dietro a questa disciplina, quali saranno le innovazioni tecnologiche che potremmo raggiungere grazie al Machine Learning?

------
