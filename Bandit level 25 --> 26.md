# Comandi usati:
	ssh
	cat
	exit
	chmod
# Procedura:
	ssh bandit25@bandit.labs.overthewire.org -p 2220
	cat bandit26.sshkey
	return:
		(key)
	exit
	nano bandit26key
		(key)
	chmod 600 bandit26key
	ssh -i bandit26key bandit26@bandit.labs.overthewire.org -p 2220
	(dopo aver ridotto la finestra, per far bloccare --More--)
	v
	:set shell=/bin/bash
	:sh
	cat 
	
	(quando entri in bandit26, la shell non è /bin/bash, ma uno script che avvia 
	il programma more che mostra un testo, e chiude la connessione. Riducendo la 
	finestra, more si interrompe, allora si può premere v e impostare la shell 
	come /bin/bash, aggirando il sistema)
# Password sbloccata:
	jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ