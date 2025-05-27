
# GRADINATA ROVERETO
Repository per il progetto in Blender di Trabucco Luigi (FCG)

Il progetto consiste nella realizzazione di un modello 3D del logo di una tifoseria organizzata creata dal sottoscritto e alcuni amici, la Gradinata Rovereto.
Siamo un gruppo Ultras che segue una squadra di basket Chiavarese che milita in 6a serie nazionale.
Il progetto è realizzato usando la versione 4.3.2
Il Disegno è stato realizzato da un amico perciò non ho trovato reference utilizzabili su internet.
Prima di seguire il corso di Fondamenti di Computer Grafica mi ero già interessato a Blender, con l'obiettivo di creare modelli stampabili (al tempo con scarsi risultati).

![Image](https://github.com/user-attachments/assets/583d0e2d-e048-47b2-b265-70f56ac1df94)

# ORGANIZZAZIONE REPOSITORY 📂
Nella repository sono presenti 5 Cartelle contenenti tutti i file indicati su questo README.
Ho deciso di scomporre il mio modello principale in 3 modelli differenti (folder chiave/spada/elmo), tutto il lavoro svolto poi sui 3 modelli congiunti si trova nel folder "finale", mentre nel folder "render" si trovano tutti i render del mio progetto.

# SPADA 🗡
Ho cominciato la mia modellazione a partire dal modello della spada. Non avendo modelli da cui partire ho importato direttamente sulla mia view di lavoro l'immagine del modello per intero, così da seguire con precisione il disegno.

1. Sono partito da un cubo che, dopo aver scalato, ho posto alla stessa misura della mia immagine, dopo averlo scalato sull'asse x e aver aggiunto dei loop cut. Dopodichè ho rialzato i due edges che corrispondevano ai "pomelli" e ho fatto un bevel (Ctrl+B) simmetrico selezionando entrambi i lati insieme, così da aver una forma arrotondata. ***spada_1.blend***

2. Successivamente ho fatto un Insert (I) sulle facce centrali così da centralizzare i miei nodi. Poi ho selezionato i lati che comporranno la mia lama per poterli estrudere verso l'alto fino all'altezza del disegno. ***spada_2.blend***

![image](https://github.com/user-attachments/assets/f04191a6-a2d4-43ee-8222-9d3e9c822371)

3. a questo punto o preso tutti i vertici della punta della mia spada e li ho uniti centralmente in un unico vertice per avere appunto la punta della spada che poi ho posto in corrispondenza della punta nel disegno. ***spada_3.blend***

![image](https://github.com/user-attachments/assets/73e887ea-58f4-432e-aaa4-ca0376edc00b)

4. dopo aver pensato alla lama mi sono occupato dell'impugnatura. Per l'impugnatura ho semplicemente utilizzato un cilidro a cui ho aggiunto un certo numero di facce così poi, anche con il *subdivision modifier* e il *Shade auto smooth* risultasse liscio e senza facce squadrate.
dopodichè ho scalato il fondo utilizzando il *Proportional editing* per rispettare il disegno, per fare il "pomello" finale ho utilizzato un altro cilindro che ho trattato come il manico a cui ho fatto un bevel per arrotondarne i lati. ***spada_4.blend***

![image](https://github.com/user-attachments/assets/1c52c076-050e-4a9f-b2cb-8c5b1e8d4485)

5. Infine mi sono occupato dei particolari, ad esempio ho assottigliato maggiormente la lama e ho sistemato il "bloccadita" che aveva alcune imperfezioni, tra cui un bevel fatto due volte che creava delle imperfezioni. Ultimo ma non ultimo ho unito tutte le mash in una unica così da provare un minimo di sculpting. ***spada_5.blend***

6. Utilizzando lo strumento *brush* ho provato a dare colore al modello così da provare anche un primo rendering, ho preso dimestichezza con l'utilizzo e su come creare un materiale partendo dallo strumento brush (successivamente rivalutato). ***spada_6.blend***

![image](https://github.com/user-attachments/assets/8c528481-3d20-4266-9b5e-580b0109549e)

7. infine ho creato un semplice setup per provare ad acquisire un immagine impostando uno sfondo e una luce (non avevo ancoa tenuto in considerazione la parte di shading).
Il setup si trova nel file ***spada.blend***, file principale da cui ho salvato i passaggi intermedi. Il primo render è stato questo. **spada_render.png**

![spada_render](https://github.com/user-attachments/assets/7d370592-d2e5-431e-a639-3f90ecc62864)

# CHIAVE 🗝
Per la modellazione della chiave ho utilizzato la stessa tecnica per la spada, ho importato in blender il mio disegno così da seguire al meglio il modello (anche perchè del disegno a mano sono molto carente di qualità).

1. Sono partito da un cilindro che ho posto esattamente sul disegno e della stessa misura. Inizialmente ho fatto un errore che si è propagato nel corso della modellazione, infatti ho lasciato l'immagine di riferimento "dritta", quindi con la chiave obliqua, mi ha creato non pochi problemi soprattutto con la gestione delle estruzioni ma me la sono cavata lo stesso.
Il cilindro iniziale dopo aver inserito un *subdivision modifier* e un *Shade auto smooth* è stato estruso per la lunghezza della chiave. Successivamente ho estruso più volte utilizzando anche il *Proportional editing* per ottenere la stessa forma mostrata in figura. ***chiave_1.blend***

![Screenshot 2025-05-26 112329](https://github.com/user-attachments/assets/ef2e3474-2de7-4050-b8db-030155b4b9f5)

2. Mi sono occupato poi dell aparte più complicata dell'oggetto, la fine della chiave.
Guardando online ho visto che, per fare corde/fili/tubi ..., si utilizzava il *NurbsPath* così ho deciso di utilizzarlo.
Dopo aver estruso varie volte e aver unito i due lembi, ne è risultato un ciclo che ho scalato rispetto all'immagine di riferimento.
Rispetto all'immagine non è precisissima la parte centrale poichè nel caso avessi spostato troppo i nodi in alcuni punti si sovrapponevano e non ero pronto ad affrontare le sovrapposizioni già all'inizio, ho preferito quindi rendrlo più semplice ma comunque di effetto. ***chiave_2.blend***

![image](https://github.com/user-attachments/assets/c8c52d0c-ad21-40f8-a6b4-ece4b2a8e041)

3. Dopodichè ho unito "l'asta" della chiave al mio NurbsPath estrundendo ancora l'asta, ho convertito il NurbsPath e l'ho sistemato. Dopo averlo reso una mash sono riuscito a modificarlo meglio così de renderlo più simile al disegno. ***chiave_3.blend***

4. Mi sono occupato poi della vera e propria parte per aprire la nostra porta. Ho utilizzato un piano che ho scalato e sistemato in corrispondenza del disegno. Ho utilizzato lo strumento *knife* per creare i tagli, inizialmente avevo pensato di utilizzare un modificatore specchio (che conoscevo già per la modellazione da stampa) ma mi piaceva che tutti i tagli non fossero uguali tra loro. Ho avuto qualche problema iniziale sull'uso dello strumento knife perchè non mi ero reso conto delle shortcut in basso nello schermo che permettevano di aggiungere delle funzionalità indispensabili, quali ad esempio il *cut throwh* (C). ***chiave_4.blend***

![image](https://github.com/user-attachments/assets/6fe283f5-27d7-4aca-b1b7-93d29c5159e9)

5. A questo punto mancava solo la punta della nostra chiave, ho utilizzato la stessa tecnica iniziale, ho quindi fatto delle estrusioni e degli insert successivi fino ad avere la forma desiderata. ***chiave_5.blend***

6. La mia idea iniziale era di avere, alla fine del progetto, una animazione con il vento, ho quindi cominciato a vedere online strumenti per creare al meglio i vestiti. Ho trovato ed utilizzato una *Curva di Bézier* andando a creare un piccolo drappo sul fondo della chiave. Ho provato poi a creare una piccola animazione. ***chiave_6.blend***

![image](https://github.com/user-attachments/assets/9ee44912-9df8-4f76-a80d-24c7d7cb7d33)

7. Questo è il punto in cui inizialmente mi sono bloccato maggiormente, facevo partire le animazioni e il drappo spariva, da li ho cominciato a comprendere il concetto di modificatore *Cloth* e *Collision*. Sono riuscito a creare una animazione ma il mio drappo sgusciava via dopo qualche frame. Ho deciso quindi, per rendere più reale il drappo, di far partire l'animazione e di creare una mash relativa nel mezzo dell'animazione, (ho deciso di occuparmi dell'animazione alla fine, non avevo ancora le conoscenze adatte). ***chiave_7.blend***

![image](https://github.com/user-attachments/assets/5920f833-77c2-4862-8a20-2515a6fd49c7)

8. A questo punto, finita la modellazione, ho cominciato come per la spada ad utilizzare il brush per dare un pò di colore. ***chiave_8.blend***

![image](https://github.com/user-attachments/assets/cb58c473-ae95-447a-a0a9-6f19b159b485)

9. Ho colorato anche il drappo andando a selezioneare le singole facce che volevo blue e le singole facce ch volevo gialle (scoperto successivamente che era il modo più sbagliato).
Ho provato anche ad aggiungere delle obre e dei punti di luce con il pennello ma il risulatto non mi piaceva un granchè. ***chiave_9.blend***

![image](https://github.com/user-attachments/assets/84caa690-7169-43dc-a0ff-529f0bd2579b)

10. Nel mentre che spennellavo mi sono imbattuto in alcuni valori del mio modello, ovvero la *Roughtness* e *Metallic* modificandoli un pò ho ottenuto il risultato che volevo inizialmente. ***chiave_10.blend***
    
11. Nel file ***chiave.blend*** si trova il setup per il render dell'immagine della chiave ed è anche il file che ho utilizzato per tutta la realizzazione del modello.

![chiave_render](https://github.com/user-attachments/assets/311d079a-a890-4753-afc3-29498885e9e6)

# ELMO 🛡

Per l'elmo non ho utilizzato l'immagine di riferimento poichè non essendo abbastanza dettagliata e senza un buon riferimento degli spazi sarebbe stato inutile. Ho trovato però su youtube un video di una modellazione di un elmo e ne ho preso ispirazione. [link al video](https://www.youtube.com/watch?v=yV5Kl4o13VE&t=149s)

1. Questa volta ho subito impostato per bene le dimensioni e la posizione del mio oggetto iniziale (un cubo) così da non avere problemi in seguito.
Il mio cubo iniziale ha subito un Bevel su 3 dei 4 lati esterni così da lasciare solo una "punta" ovvero la parte d'avanti dell'elmo.
Dopodichè ho fatto un loop cut *Ctrl+R* attorno alla mia figura e l'ho sistemata all'altezza degli occhi, dopodichè ho scalato il taglio così da creare la mia forma di partenza.
Dopo aver "lisciato" le facce utilizzando i soliti modificatori, ho tagliato la testa del mio modello così da creare la placca superiore dell'elmo, ho utilizzato lo strumento *knife* e poi ho modellato la placca scalando e facendo delle estrusioni per rendere la figura più interessante. ***elmo_1.blend***

![image](https://github.com/user-attachments/assets/125e1aa5-7e93-4201-9ddf-66e636a3071c)

2. A questo punto, visto che non avevo una reference precisa (il disegno iniziale è di vista frontale), ho inventato il retro, seguendo anche il video linkato il quale usa delle funzionalità a pagamento per modellare e quindi mi sono dovuto reinventare.
Ho diviso in due metà il pezzo principale e ho scalato quello posteriore così da dare l'effetto di due pezzi saldati insieme, ho poi tagliato in modo obliquo quello anteriore così da rendere più interessante il modello. ***elmo_2.blend***

![Screenshot 2025-05-26 122059](https://github.com/user-attachments/assets/31f4b4ee-b2b6-4ad4-8919-fea22112162a)

3-4. Utilizzando lo strumento *Knife* ho tagliato a "croce il modello sul davanti, prima tagliando per gli occhi e poi per la placca frontale. Anche in questo caso inizialmente ho avuto qualche difficolta con lo strumento ma con un pò di pratica ho avuto i miei tagli. ***elmo_3.blend*** - ***elmo_4.blend***

![image](https://github.com/user-attachments/assets/718f20a7-f5d2-4d88-b0c1-b1eb155b05d4)

5. A questo punto volevo estrudere verso l'esterno il taglio degli occhi e quello della placca frontale, ho avuto molte difficolta inizialmente perchè le mie estrusioni seguivano sempre un asse, ma io volevo che estrudesse seguendo la figura.
Dopo varie ricerche ho scoperto che potevo *estrudere sulla normale* e quindi risolvere il problema di estrusione.
Dopodichè ho fatto un bevel dei lati della placca degli occhi. ***elmo_5.blend***

![image](https://github.com/user-attachments/assets/10e75cc4-6ce7-435e-9d79-74a2a0933ab9)

6. Ho fatto anche i tagli per gli occhi, sempre con lo strumento *knife*, dopodichè ho fatto un bevel per l'interno del taglio.
Un problema che ho avuto e stato quello di ritrovarmi con una grande quantità di edges inutili, creati dal bevel, quindi li ho "ripuliti" eliminando quelli non necessari. ***elmo_6.blend***

![image](https://github.com/user-attachments/assets/c19e4178-3329-4a0f-8a01-e741ca69e524)

7-8-9-10. A questo punto ho aggiunto i rivetti dell'elmo, ho usato diverse tecniche, di cui una suggerita nel video linkato sopra.
Pre prima cosa un rivetto è semplicemente una sfera con un *subdivision modifier* e un *Shade auto smooth*, i primi che ho inserito sono quelli laterali che uniscono la placca frontale con quella posteriore, ho utilizzato un modificatore *Mirror* così da posizionarli solo su un lato.
Poi mi sono occupato di quelli sulla placca superiore, per prima cosa ho fatto un loop cut che circondasse tutta la placca, perfettamente centrato sul lato della placca, linea immaginaria di dove andranno i rivetti. Dopodichè ho selezionato tutti gli edges partendo dal primo e premendo *Ctrl* su quello centrale per selezionare anche tutti gli intermedi e li ho separati dal resto del modello.
Ho utilizzato i *Geometry Nodes* sulla line appena separata, inserendo un *Istance on Points* e selezioanndo come istanza il rivetto. Per gestire poi il numero di rivetti ho aggiunto un *resample curve* così da gestire il numero di rivetti, a questo punto aggiungiamo un modificatore *Mirror* per l'altro lato della placca.
Infine, "a mano", ho aggiunto i rivetti attorno agli occhi e sulla placca frontale, sempre utilizzando *Mirror*.
- ***elmo_7.blend*** rivetti di unione tra le due placche principale 
- ***elmo_8.blend*** rivetti sulla placca superiore
- ***elmo_9.blend*** rivetti sulla placca frontale
- ***elmo_10.blend*** rivetti sugli occhi

![image](https://github.com/user-attachments/assets/b24d49c0-9c43-49a9-a70b-43cc04d78e6a)

11. Dopo aver completato la struttura dell'elmo mi sono preoccupato della sciarpa. Ho impiegato una grande quantità di tempo per capire quale tecnica utilizzare visto anche il fatto di non avere una figura sottostante (collo e spalle) su cui far poggiare la sciarpa, infatti ho deciso di lasciarla fissa e di asseganre il modificatore *Cloth* solamente al lembo di sciarpa che fuoriesce.
Per creare la sciarpa ho utilizzato quindi una *Curva di Bézier*. ***elmo_11.blend***

![image](https://github.com/user-attachments/assets/d91adfb9-d14d-4f16-8147-5dd16fe41cb5)

12. Subito dopo ne ho sistemato la forma e la struttura, agigugnendo delle suddivisioni e aumentando, nella sezione *Geometry* dell'oggetto, il valore di *Extrude* e, nella sezione *Bevel*, il valore di *Depth* così da raggiungere la forma desiderata. ***elmo_12.blend***

13. Mi sono occupato poi del pezzo di sciarpa pendente, siccome nella mia animazione voglio che sia lei a sventolare è un oggetto diverso rispetto al resto della sciarpa così da non avere problemi in seguito.
Utilizzando sempre una *curva di Bézier* ho creato la sciarpa, ne ho tappato i buchi dopo averli dato una dimensione (*Fill Caps*) e poi lo convertita in una mash, così come la curva precedente per la parte statica della sciarpa. ***elmo_13.blend***

![image](https://github.com/user-attachments/assets/4db9942a-3c71-4e73-8d29-7f5e00840675)

14. Infine, grazie anche ad una buona dose di studio e ricerca online tra youtube e blog, ho cercato di comprendere il funzionamento delle animazioni con i *cloth* e i vari parametri. Di seguito una delle prove con anche un problema che avevo riscontrato con il tappo finale della sciarpa che si staccava dal resto della mash, risolto semplicemente ricostruendo le facce che lo componevano. ***elmo_14.blend***

https://github.com/user-attachments/assets/68464c4c-b39a-47ec-8f69-ad8f931104d7

Sul file ***elmo.blend*** si trova il modello dell'elmo finito ed è il file che ho utilizzato per tutto il modello e per creare i salvataggi intermedi

# FINALE 🏁

1. Dopo aver creato i 3 modelli il risultato è il seguente. ***finale_1.blend***
Ho deciso di "buttare" il lavoro fatto di sculpting con i colori, non ne ero soddisfatto e sono ripartito dai modelli con il materiale di base e mi sono messo a studiare attraverso diversi video e forum, il mondo dello shading e della realizzazione dei materiali.
Dal mio punto di vista la parte dei materiali è molto complicata ma allo stesso tempo affascinante, sicuramente in futuro ne approfondirò le peculiarità.

![image](https://github.com/user-attachments/assets/9acc460f-2d71-45ed-9040-34e19845463c)

2. Ho ripreso l'immagine di partenza e ho allineato i modelli come nell'immagine, (purtroppo ho dovuto sovrapporre la spada e la chiave in un punto). ***finale_2.blend***

![image](https://github.com/user-attachments/assets/21dc10a6-9cd5-46ff-b89f-67db436c94a2)

3-4. Come prima cosa ho provato la funzionalità del *vento*, con scarsi risultati. Leggendo online ho capito che la funzionalità del vento è difficile da gestire dati i molti fattorri che potrebbero causare il non funzionamento, decido di affrontarlo in seguito. Nel mentre ho sistemato la sciarpa pendendte che ora è molto più realistica. ***finale_3.blend*** - ***finale_4.blend***

![image](https://github.com/user-attachments/assets/2669ae52-e030-4d98-97ff-ee650dd79cc6)

5. Ho cominciato anche  apensare ad una possibile animazione differente da quella del vento, nel caso non fossi riuscito a farla funzionare. Ho creato una piccola animazione con la figura che gira di 360 gradi. Non mi ha emozionato e l'ho sccessivamente scartata. ***finale_5.blend***

6. Dopo la fallimentare prova di animazione ho ricominciato la parte di shading e colorazione. Ho cominciato ad assegnare diversi materiali base alla mia figura, non più utilizzando la funzionalità Brush ma con la creazione di materiali. ***finale_6.blend***

![image](https://github.com/user-attachments/assets/94eec815-d77a-47ee-909e-593651295038)

7-8. Ho cominciato a lavorare sulla finestra di *shading* e ho lavorato sulle shader della chiave e della spada seguendo dei consigli di un forum. Ho aggiunto una *Color Ramp* al mio materiale *chiave* così da avere un cambio di color con la variazione della luce sull'oggetto. Da giallo scuro (oggetto non illuminato) a bianco (oggetto illuminato diretto) ***finale_7.blend*** - ***finale_8.blend***

![image](https://github.com/user-attachments/assets/ec8d1031-d2e8-4fef-b27d-5002b7cbfb01)

9. Ho utilizzato la stessa tecnica in tutte le porzioni dell'elmo, dai rivetti alle placche, cercando di mantenere il colore iniziale. ***finale_9.blend***

![image](https://github.com/user-attachments/assets/5ae4d076-cd0e-43f8-903d-5083d7c40150)

10. come ultima cosa ho diviso la spada (che era una mash unica) nei diversi pezzi che la compongono. Ad ogni pezzo poi ho assegnato il relativo materiale sempre settato con una *Color Ramp* per la luce. ***finale_10.blend***

![image](https://github.com/user-attachments/assets/3a780b86-7f69-4744-8498-9243c9dd4da4)

11. Mancava la sciarpa e il drappo della chiave, per non fare l'errore della prima volta che avevo colorato selezionando ogni porzione a mano, ho cercato online e mi sono inbattuto in un video che spiegava tutti gli 80+ nodi per i materiali su blender. Visto anche che da li a poco avrei lavorato sui materiali ho deciso di guardarlo per intero. [link al video](https://www.youtube.com/watch?v=cQ0qtcSymDI&t=401s)

Tra i vari nodi ho individuato *Wave Texture* che unito ad un *Color ramp* con i miei due colori mi ha permesso di avere la mia sciarpa bi-color. Ho usato lo stesso materiale creato per tutte le parti con quel pattern andando di volta in volta a sistemare l'orientamento delle linee, la grandezza e la quantità.
***finale_11.blend***

![Screenshot 2025-05-26 151932](https://github.com/user-attachments/assets/27f95ad3-7b50-4fa3-95a6-bcba33e8b8c7)

12. Finito il colore della sciarpa non ero soddisfatto dall'effeto, sembrava un pezzo di metallo più che una sciarpa. Seguendo sempre il video linkato sopra ho provato un pò di nodi differenti fino a trovare *Noise Texture* e *bump*, il primo crea, appunto, delle imperfezioni sulla mash, mentre bump le fa ,più o meno, risaltare. ***finale_12.blend***

![image](https://github.com/user-attachments/assets/9e782a94-62d2-4352-9a80-a94ef82b041f)

13. Andando avanti con i materiali ho provato a ricreare un effetto "pellato" per l'impugnatura della spada. Dopo un pò di tentativi non avevo creato un materiale che mi piacesse quindi cercando su youtube ho trovato il canale di un ragazzo che realizza materiali procedurali, da cui mi sono ispirato anche per i materiali successivi.
[link al canale](https://www.youtube.com/@3dpunk)
Il risultato dopo aver visto i suoi video è stato il seguente. ***finale_13.blend***

![image](https://github.com/user-attachments/assets/6d7598ea-ac6e-4396-9ab7-ab86faa2b28e)

14. Sul canale linkato ho trovato un sacco di materiali interessantissimi e perfetti per il mio progetto. Ho cercato di creare un mio materiale per la spada dopo aver visto il suo video. Inizialmente è stato molto difficile comprendere alcuni tipi di nodi m andando avanti si cominciano a comprendere. Risultano essere solo una successione *Noise Texture* e *Varanoi Texture* che intervallate da *Color ramp* e *Bump* restituiscono l'effetto desiderato.
Senza una conoscenza approfondita dei materiali è quasi impossibile creare un materiale realistico per questo ho preso molta ispirazione dal ragazzo dei video e cercando poi di modificali a mio gusto anche per prendere dimestichezza e per capire i vari modificatori di ogni nodo.
L'effetto finale della spada è il seguente. ***finale_14.blend***

![Screenshot 2025-05-26 153715](https://github.com/user-attachments/assets/a9b5927c-fa00-4e1c-b0d7-9158086c29a1)

![image](https://github.com/user-attachments/assets/e8842f24-4854-496e-9578-01b1d677e2ed)

15. Mi sono occupato poi del materiale della chiave, facendomi ispirare dal suo video su un materiale *oro* perfetto per la chiave.
Rispetto al suo materiale ho cercato di rendere la chiave più sporca inserendo molte più *Noise Texture* e più rampe di colore diverse, anche più verso l'arancione. ***finale_15.blend***

![image](https://github.com/user-attachments/assets/e100ed86-10a1-497e-8379-eb85a97b0676)

16. Sono passato poi all placca *base*, questo il nome del materiale, utilizzato anche sulla spada, ho cercato un materiale simile a quello della spada ma molto più rovinato. ***finale_16.blend***

![image](https://github.com/user-attachments/assets/5c00a1d2-0b19-4a52-bf63-84955dc9e752)

17. Come ultima cosa ho copiato lo stesos materiale usato nelle placche rpincipali, l'ho leggermente modificato rimuovendo alcuni *Noise Texture* e l'ho reso del colore desiderato. Materiale che è assegnato a tutti i rivetti e alla placca frontale. Guardando il disegno mi sono anche reso conto che questo materiale andava assegnato anch alla faccia superiore della placca superiore e così ho fatto. ***finale_17.blend***

![image](https://github.com/user-attachments/assets/b95ad5d3-630d-41d4-908f-0e01e239f553)

Giunto alla fine dell'editing dei materiali ho creato una scena e aggiustato le luci, ho utilizzato dei piani che ho scalato e posizionato a mio gradimento, ho impostato un colore e sezione dei materiali ho impostato la *Surface* come *Emission* così da avere della luce di quel colore. Ho settato anche la telecamera davanti al modello che si trova all'interno della scena costruita con dei "muri" neri così da non avere uno sfondo e poter giocare con le luci.
Il file finale con il set up del rendering si trova nel file ***finale.blend***

![image](https://github.com/user-attachments/assets/eb7bf072-3dae-418e-a813-6bee18e1b3ed)

# RENDERING 🎥 📷

### Animazione del vento
Per prima cosa ho riaffrontato il problema del vento, questa volta con dei risultati. Ho guardato una grande quantità di video di perosne che creavano delle bandiere al vento (non li linko tutti, sono veramente tanti) cercando di capire il perchè del  mio mancato funzionamento.
Con calma studiando nel pannello *Physics* del vento ho trovato il problema. Non stavo dando abbastanza forza al vento il quale non spostava di un millimetro la mia sciarpa. Questo il risultato finale.

https://github.com/user-attachments/assets/af1131f9-73a2-4dbf-8c6e-ee4115ec6fed

### Primo rendering di un'immagine
Ho eseguito il primo rendering con **2048 Samples** (decisamente troppi) e come render engine ho usato *Cycles*, molto buono per rappresentare le obre ma molto pesante da elaborare l'immagine. Il risultato è stato il seguente. ***Render.png***

![Render](https://github.com/user-attachments/assets/9db0cade-0aa2-4387-8e02-34575b83c6ae)

### Secondo rendering di un'immagine
L'effetto mi piaceva molto, non è fedele all'immagine ma le due metà illuminate mi piacevano molto. Unica pecca è che mancava una luce chiara che illuminasse per bene il davanti e la spada e la chiave così l'ho aggiunta e questo è il risultato con **50 Samples** (decisamente pochi ma volevo testare la qualità per poi gestire al meglio la renderizzazione dell'animazione. ***render_50.png***

![render_50](https://github.com/user-attachments/assets/2c5922cf-551c-4f3e-a559-4157ee3f486f)

### Rendering Video
Ho creato una semplice animazioen di vista frontale con 50 Samples di qualità e un totale di 125 frame (con 25 frames al secondo), il risultato è il seguente. La qualità dell'immagine non è un granchè ma ho dovuto abbassare i sample altrimenti la durata della renderizzazione sarebbe stata eccessiva.

https://github.com/user-attachments/assets/5c7e4307-4be1-4a01-bcba-488312dfdb2a















 





























   
