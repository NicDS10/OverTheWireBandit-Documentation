# Linux commands
- / : se preso singolarmente indica l'intero sistema
- man : guida su uno specifico comando
- clear : pulisce il terminale
- exit : esce dal server o dalla macchina a cui sei collegato
- pwd : indica la cartella in cui ti trovi
- "" : il testo racchiuso quì dentro viene preso come tale annullando vari comandi speciali

[[Bandit level 0 --> 1]]
- ssh : permette di collegarti ad un server remoto tramite SSH (secure shell), con -i ti colleghi tramite un file senza password, mentre con -p specifichi la porta                
- ls : legge e mostra tutti gli elementi della cartella (directory) in cui ti trovi. Se aggiungi l'opzione -a, indichi di elencare tutti i file, anche quelli nascosti           
- cat : legge e mostra il contenuto di un file            

[[Bandit level 01 --> 2]]
- `-` : da solo indica lo standard input, ovvero che non leggi nessun file, ma quello che scrivi da tastiera lo rispedisci a schermo (per uscire Ctrl + C). Prima di altre lettere, come -a, va a modificare il comportamento di un comando                                         
- ./'filename' : il . prende la cartella corrente e / indica che ciò che si inserisce dopo verrà preso come nome di un file, anche -                  

[[Bandit level 02 --> 3]]
- `\` : l'escape, elimina il significato del carattere speciale successivo. Utile quando si incontrano spazi nel nome di un file, che dividono il file come se ce ne fossero più di uno. `\` va a eliminare il valore speciale dello spazio di divisore             
- -- : se messo prima di specifici comandi, fanno da opzioni lunghe, che svolgono lo stesso ruolo delle opzioni corte ma con parole intere, per esempio  -a  -->  --all. Se messo da solo indica che tutte le opzioni e i flag finiscono lì             

[[Bandit level 03 --> 4]]
- cd : ti permette di spostarti in un'altra directory         

[[Bandit level 04 --> 5]]
- file : indica la tipologia dei file indicati                       

[[Bandit level 05 --> 6]]
- find : trova un file in una directory con date qualità (-type f significa file regolare, -size 1033c significa di 1033 bit e ! -executable significa non eseguibile, -user per indicare l'utente che lo possiede, -group il gruppo che lo possiede ecc)                      

[[Bandit level 06 --> 7]]
- 2>/dev/null : se messo nel file, significa che tutti gli errori, ovvero gli accessi negati presenti nel canale 2, invece di venire a schermo vengono reinderizzati nel vuoto       

[[Bandit level 07 --> 8]]
- grep : cerca dei pattern in dei file, per esempio grep (parola) (filename) restituisce le righe in cui si trova quella parola nel file                           

[[Bandit level 08 --> 9]]
- sort : prende tutte le righe di un file e le mette in ordine alfabetico  
- | : pipe, collega due comandi, e spedisce l'output di uno nell'altro       
- uniq : cerca o omette le linee duplicate, confrontando una riga con la successiva; con -u va a scrivere le righe che si ripetono una sola volta, ma confrontate solo alla succesiva (è necessario sort | per cercare nell'intero file)             

[[Bandit level 09 --> 10]]
- strings : scrive tutti i caratteri scrivibili e quindi non corrotti di un file        

[[Bandit level 10 --> 11]]
- base64 : codfica il testo di un file in base64; con il flag -d decodifica in testo normale     

[[Bandit level 11 --> 12]]
- tr : scambia tutti i caratteri di un file in base alle tue indicazioni, per esempio 'a-z' 'A-Z' 

[[Bandit level 12 --> 13]]
- tar : impacchetta uno o più file in un archivio, quindi mette dei file in un altro file. Per estrarreda quel file, è utile -xvf, con x per estrai, v per scrivi quello che hai estratto e f (che va sempre per ultimo) per indicare il nome del file da cui vuoi estrarre.      
- gzip : comprime file, con -d li decomprime       
- bzip2 : identico a gzip, ma comprime e decomprime in modo diverso         
- xxd : converte file in hex dump, utile quando si hanno file compressi e si vogliono rendere esadecimali; con -r trasformi da esadecimale al file compresso in questo caso            
- mkdir : crea una directory col nome dato    
- mktemp : crea un file (o una directory con -d) con nome casuale        
- mv : rinomina un file per esempio con il nome dato, utile quando si vuole aggiungere un'estensione per comprimere o decomprimere file             
- cp : copia file da una cartella a un'altra (si deve indicare il percorso completo, ma si può usare . per indicare la corrente)                   

[[Bandit level 13 --> 14]]
- scp : ti permette di copiare un file dal web via OpenSSH, con -P specifichi la porta      
- chmod : cambia la modalità del/i file specificati, con 600 permette al proprietario di leggerlo e scriverci, bloccando i permessi a chiunque altro di fare qualsiasi cosa con il file  

[[Bandit level 14 --> 15]]
- nc : utilissimo per mandare file e ricevere risposte (o no se la porta non risponde) senza crittografia, e sia alle porte TCP che UDP. Utile anche con -l per metterlo in ascolto su una porta e vedere se qualcuno prova a connettersi                                  
- telnet : si connette solo a porte TCP, non ha modalità ascolto ma serve unicamente a verificare se una porta risponde o no                        

[[Bandit level 15 --> 16]]
- ncat : come nc, ma offre più funzionalità come il flag --ssl che ti permette di usare la crittografia ssl per connetterti ad una porta che la richiede      
- openssl s_client : il metodo standard per connettersi ad una porta con protocollo SSL/TLS; ncat --ssl fa la stessa cosa di s_client, ma spesso non è preinstallato, mentre openssl è un intera suite di crittografia che ti permette di fare molte altre cose. Per usare il comando, è necessario scrivere openssl s_client -connect `host`:`porta`, e con -quiet non fa vedere l'handshake e i certificati      

[[Bandit level 16 --> 17]]
- nmap : permette di scannerizzare molte porte di un server, una macchina o una rete, per scoprire se sono aperte, chiuse, non rispondono, e anche il tipo o il protocollo che usano con -sV. Con -T4 forzi lo scan e va molto più veloce, mentre con --open specifichi di mostrare solamente quelle aperte     
- nano : permette di creare file, come touch, ma ti mostra un editor di testo        

[[Bandit level 17 --> 18]]
- diff : confronta dei file elencando le differenze riga per riga      

[[Bandit level 18 --> 19]]
- ssh + `comando` : dopo aver fatto ssh, senza pipe, puoi aggiungere un comando che verrà eseguito, per poi chiudere subito la connessione      

[[Bandit level 20 --> 21]]
- echo : scrive una riga di testo, come print di Python, ma per leggere una variabile serve $ 

[[Bandit level 21 --> 22]]
- cron : è il programma che svolge dei compiti in automatico e in background a intervalli regolari, seguendo le tabelle crontab, che si dividono in quelle personali, senza i permessi, e quelle gestite dagli amministratori, che fanno quindi comandi con i permessi di uno specifico utente (come i file SUID, solo che questi li esegue un utente con i permessi di un altro, mentre le crontab le esegue cron in automatico)      
- crontab : sono le tabelle che dicono a cron i compiti che deve eseguire, che si chiamano cronjob. In un file crontab si trovano  * * * * * , che indicano rispettivamente minuto, ora, giorno del mese, mese e giorno della settimana (con la , si specifica un elenco, con il - un intervallo e con / una frequenza tipo `*/15`), e se lasciati così e non sostituiti da numeri i comandi vengono svolti ogni minuto (sennò si può mettere tipo sleep 30 secondi per fare eseguire una parte dopo 30 secondi e quindi è come se andasse a quell'intervallo); i permessi, che indicano l'utente i cui permessi vengono usati per eseguire i comandi, e gli effettivi comandi, che possono essere anche file che vengono eseguiti. Con &> /dev/null non si fanno leggere messaggi a schermo       
- &> : gestisce i flussi di testo, prendenso sia l'output normale che gli errori     

[[Bandit level 22 --> 23]]
- $ : da solo indica l'utente, ma se messo prima di una stringa indica una variabile     

[[Bandit level 23 --> 24]]
- chmod 777: dà i permessi completi di leggere, scrivere ed eseguire un file     

[[Bandit level 24 --> 25]]
- for : la funzione è come un for classico, con for _  in {0000..9999}; do ...; done, oppure a strati con un comando per riga, ma in un file. Se si vuole usare su una porta, meglio usare il primo esempio

[[Bandit level 25 --> 26]]      [[Bandit level 26 --> 27]]
- more : un programma che se avviato da uno script che si sostituisce alla shell normale, legge file di testo lunghi, e può essere fermato riducendo la finestra, in quanto non può stampare tutto in una volta sola
- vim : editor di testo avviabile con v quando si blocca more, permette di cambiare shell ed impostare la normale /bin/bash

[[Bandit level 27 --> 28]]
- git : un software che ti permette di fare version control e salvare file con commit, esplorare i salvataggi, caricarli su github dove si travano le repository, cartelle con tutti i commit, tramite push, oppure prenderli tramite pull, che sarebbe fetch + merge, creare un branch, ovvero una copia, un'altro ramo, e molto altro

	*Nei livelli 27-31 ci sono i comandi specifici

[[Bandit level 28 --> 29]]
- rm : permette di rimuovere file o cartelle, con -rf rimuovi le cartelle e tutto il loro contenuto in modo forzato

[[Bandit level 29 --> 30]]
- git log --all --oneline --graph : utile per avere più informazioni possibile sulla storia di una repository, in quanto elenca tutti i commit, tutti i branch, mostra solo la parte iniziale dell'hash e con dei simboli mostra i merge, le ramificazioni ecc

[[Bandit level 30 --> 31]]
- git tag : elenca i tag, ovvero  delle milestone che puntano sempre ad un commit e possono indicare il completamento della prima parte di un progetto per esempio
- git fsck --lost-found : chiedi a git di scansionare tutto il database della repository, per trovare i cosiddetti "oggetti orfani" (o "dangling objects"), che non sono collegati a nessun ramo (branch) e non sono quindi raggiungibili tramite log o tag

[[Bandit level 31 --> 32]]
- git add : aggiunge un file all'index, con -f ignora il .gitignore
- git commit -m : fa un commit, un salvataggio di tutti i file, e richiede anche un messaggio per specificare i cambiamenti
- git push : prende i commit e li invia alla repository, specificando il branch

[[Bandit level 32 --> 33]]
- $0 : fa riferimento sempre al comando o script in esecuzione, ovvero /bin/bash in questo caso (la shell), ma non eredita gli specifici programmi che avvia, quindi in questo modo ho avviato una sotto-shell normale da cui digitare i comandi
- whoami : indica il nome dell'utente, come id ma più limitato

# Terminologia utile
- socket : quando ci si connette ad un server suuna porta, si crea una connessione tra due socket, ovvero uno proprio, con il proprio indirizzo ip + la propria porta di rete, e uno del server, con l'ip del server e la porta del server. Se ci si connette al localhost, ovvero alla stessa macchina (stesso pc o stesso server) a cui si è connessi, il proprio indirizzo ip sarà 127.0.0.1     [[Bandit level 14 --> 15]]

- shell di login interattiva : quando ci si connette via ssh ad un server per esempio, gli si sta chiededo di aprire una shell di login interattiva, dove puoi interagire con il sistema operativo scrivendo comandi. Se dopo ssh aggiungi un comando (senza pipe), quei file non si avviano (vale la stessa cosa se copi un file via scp)     [[Bandit level 18 --> 19]]

- SUID binary : un file che contiene al suo interno un programma che viene eseguito sempre con i permessi del proprietario, quindi che chiunque può eseguire e fare una specifica azione come fossi l'altro utente. In questo specifico caso, permette anche di eseguire i comandi messi dopo di esso come fossi il proprietario, ma non vale sempre     [[Bandit level 19 --> 20]]

- demone : processo in background che viene eseguito senza azioni da parte dell'utente, e sopravvive alla chiusura del terminale     [[Bandit level 21 --> 22]]

*Bandit level x --> y indica dove ho incontrato il comando o il termine per la prima volta