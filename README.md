
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














   
