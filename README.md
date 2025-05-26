
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
6. Utilizzando lo strumento *brush* ho provato a dare colore al modello così da provare anche un primo rendering, ho preso dimestichezza con l'utilizzo e su come creare un materiale partendo dallo strumnto brush. ***spada_6.blend***
![image](https://github.com/user-attachments/assets/8c528481-3d20-4266-9b5e-580b0109549e)
7. infine ho creato un semplice setup per provare ad acquisire un immagine impostando uno sfondo e una luce (non avevo ancoa tenuto la questione delle shader).
Il setup si trova nel file ***spada.blend*** file principale da cui ho salvato i passaggi intermedi è il primo render è stato questo. **spada_render.png**
![spada_render](https://github.com/user-attachments/assets/7d370592-d2e5-431e-a639-3f90ecc62864)






   
