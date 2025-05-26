
# GRADINATA ROVERETO
Repository per il progetto in Blender di Trabucco Luigi (FCG)

Il progetto consiste nella realizzazione di un modello 3D del logo di una tifoseria organizzata creata dal sottoscritto e alcuni amici, la Gradinata Rovereto.
Siamo un gruppo Ultras che segue una squadra di basket Chiavarese che milita in 6a serie nazionale.
Il progetto è realizzato usando la versione 4.3.2
Il Disegno è stato realizzato da un amico perciò non ho trovato reference utilizzabili su internet.
Prima di seguire il corso di Fondamenti di Computer Grafica mi ero già interessato a Blender, con l'obiettivo di creare modelli stampabili (al tempo con scarsi risultati).

![Image](https://github.com/user-attachments/assets/583d0e2d-e048-47b2-b265-70f56ac1df94)

# ORGANIZZAZIONE REPOSITORY
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

7. infine ho creato un semplice setup per provare ad acquisire un immagine impostando uno sfondo e una luce (non avevo ancoa tenuto la questione delle shader).
Il setup si trova nel file ***spada.blend***, file principale da cui ho salvato i passaggi intermedi è il primo render è stato questo. **spada_render.png**

![spada_render](https://github.com/user-attachments/assets/7d370592-d2e5-431e-a639-3f90ecc62864)

# CHIAVE 🗝
Per la modellazione della chiave ho utilizzato la stessa tecnica per la spada, ho importato in blender il mio disegno così da seguire al meglio il modello (anche perchè del disegno a mano sono molto carente di qualità).

1. Sono partito da un cilindro che ho posto esattamente sul disegno e della stessa misura. Inizialmente ho fatto un errore che si è propagato nel corso della modellazione, infatti ho lasciato l'immagine di riferimento "dritta", quindi con la chiave obliqua, mi ha creato non pochi problemi soprattutto con la gestione delle estruzioni ma me la sono cavata lo stesso.
Il cilindro iniziale dopo aver inserito un *subdivision modifier* e un *Shade auto smooth* è stato estruso per la lunghezza della chiave. Successivamente ho estruso più volte utilizzando anche il *Proportional editing* per ottenere la stessa forma mostrata in figura. ***chiave_1.blend***

![Screenshot 2025-05-26 112329](https://github.com/user-attachments/assets/ef2e3474-2de7-4050-b8db-030155b4b9f5)

2. Mi sono occupato poi dell aparte più complicata dell'oggetto, la fine della chiave.
Guardando online ho visto che, per fare corde/fili/tubi ..., si utilizzava il *NurbsPath* così ho deciso di utilizzarlo.
Dopo aver struso varie volte e aver unito i due lembi, ne è risultato un ciclo che ho scalato rispetto all'immagine di riferimento.
Rispetto all'immagine non è precisissima la parte centrale poichè nel caso avessi spostato troppo i nodi in alcuni punti si sovrapponevano e non ero pronto ad affrontare le sovrapposizioni già all'inizio, ho preferito quindi rendrlo più semplice ma comunque di effetto. ***chiave_2.blend***

![image](https://github.com/user-attachments/assets/c8c52d0c-ad21-40f8-a6b4-ece4b2a8e041)

3. Dopodichè ho unito "l'asta" della chiave al mio NurbsPath estrundendo ancora l'asta, ho convertito il NurbsPath e l'ho sistemato. Dopo averlo reso una mash sono riuscito a modificarlo meglio così de renderlo più simile al disegno. ***chiave_3.blend***

4. Mi sono occupato poi della vera e propriaparte per aprire la nostra porta. Ho utilizzato un piano che ho scalato e sistemato in corrispondenza del disegno. Ho utilizzato lo strumento *knife* per creare i tagli, inizialmente avevo pensato di utilizzare un modificatore specchio (che conoscevo già per la modellazione da stampa) ma mi piaceva che tutti i tagli non fossero uguali tra loro. Ho avuto qualche problema iniziale sull'uso dello strumento knife perchè non mi ero conto delle shortcut in basso nello schermo che permettevano di aggiungere delle funzionalità indispensabili, quali ad esempio il *cut throwh* (C). ***chiave_4.blend***

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
Il mio cubo iniziale ha subito un Bevel su 3 dei 4 lati esterni così da la sciare solo una "punta" ovvero l aparte d'avanti dell'elmo.
Dopodichè ho fatto un loop cut *Ctrl+R* attorno alla mia figura e l'ho sistemataall'altezza degli occhi, dopodichè ho scalato il taglio così da creare la mia forma di partenza.
Dopo aver "lisciato" le facce utilizzando i soliti modificatori, ho tagliato l atesta del mio modello così da creare la placca superiore dell'elmo, ho utilizzato lo strumento *knife* e poi ho modellato la placca scalando e facendo delle estrusioni per rendere la figura più interessante. ***elmo_1.blend***

![image](https://github.com/user-attachments/assets/125e1aa5-7e93-4201-9ddf-66e636a3071c)

2. A questo punto, visto che non avevo una reference precisa (il disegno iniziale è di vista frontale), ho inventato il retro, seguendo anche il video linkato il quale usa delle funzionalità a pagamento e quindi mi sono dovuto reinventare.
ho diviso in due metà il pezzo principale e ho scalato quello posteriore così da dare l'effetto di due pezzi saldati insieme, ho poi tagliato in modo obliquo quello anteriore così da rendere più interessante il modello. ***elmo_2.blend***

![Screenshot 2025-05-26 122059](https://github.com/user-attachments/assets/31f4b4ee-b2b6-4ad4-8919-fea22112162a)

3-4. Utilizzando lo strumento *Knife* ho tagliato a "croce il modello sul davanti, prima tagliando per gli occhi e poi per la placca frontale. Anche in questo caso inizialmente ho avuto qualche difficolta con lo strumento ma con un pò di pratica ho avuto i miei tagli. ***elmo_3.blend*** - ***elmo_4.blend***

![image](https://github.com/user-attachments/assets/718f20a7-f5d2-4d88-b0c1-b1eb155b05d4)

5. A questo punto volevo estrudere verso l'esterno il taglio degli occhi e quello della placca frontale, ho avuto molte difficolta inizialmente perchè le mie estrusioni seguivano sempre un asse, ma io volevo che estrudesse seguendo la figura.
Dopo varie ricerche ho scoperto che potevo *estrudere sulla normale* e quindi risolvere il problema di estrusione.
Dopodichè ho fatto un bevel dei lati della placca degli occhi. ***elmo_5.blend***

![image](https://github.com/user-attachments/assets/10e75cc4-6ce7-435e-9d79-74a2a0933ab9)

6. Ho fatto anche i tagli per gli occhi, sempre con lo strumento *knife*, dopodichè ho fatto un bevel per l'interno del taglio.
Un problema ch eho avuto e stato quello di ritrovarmi con una grande quantità di edges inutili, creati dal bevel, quindi li ho "ripuliti" eliminando quelli non necessari. ***elmo_6.blend***

![image](https://github.com/user-attachments/assets/c19e4178-3329-4a0f-8a01-e741ca69e524)

7-8-9-10. A questo punto ho aggiunto i rivetti dell'elmo, ho usato diverse tecniche, di cui una suggerita nel video linkato sopra.
Pre prima cosa un rivetto è semplicemente una sfera con un *subdivision modifier* e un *Shade auto smooth*, i primi che ho inserito sono quelli laterali che uniscono la placca frontale con quella posteriore, ho utilizzato un modificatore *Mirror* così da posizionarli solo su un lato.
Poi mi sono occupato di quelli sulla placca superiore, per prima cosa ho fatto un loop cut che circondasse tutta la placca, perfettamente centrato sul lato della placca, linea immaginaria di dove andranno i rivetti. dopodichè ho selezionato tutti gli edges partendo dal primo e premento *Ctrl* su quello centrale per selezionare anche tutti gli intermedi e li ho separati dal resto del modello.
Utilizzando i *Geometry Nodes* sulla line appena separata e inserendo un *Istance on Points* e selezioanndo come istanza il rivetto. Per gestire poi il numero di rivetti aggiungiamo un *resample curve* così da gestire il numero di rivetti, a questo punto aggiungiamo un modificatore *Mirror* per l'altro lato della placca.
Infine, "a mano", ho aggoiunto i rivetti attorno agli occhi e sulla placca frontale, sempre utilizzando *Mirror*
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
Utilizzando sempre una *curva di Bézier* ho creato la sciarpa, ne ho tappato i buchi dopo averli dato una dimensione (*Fill Caps*)




















   
