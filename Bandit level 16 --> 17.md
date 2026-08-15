# Comandi usati:
	ssh
	nmap
	ncat
	<, >
	chmod
	nano
	cat
	ls
# Procedura:
	ssh bandit16@bandit.labs.overthewire.org -p 2220
	nmap -sV -p 31000-32000
	return:
		port 31790 open SSL
	ncat --ssl localhost 31790 < /etc/bandit_pass/bandit16
	return:
		Correct!
		(private key)
	exit (da terminale privato d'ora in poi)
	nano bandit17.chiave (copiato e incollato la chiave privata senza Correct!)
	ssh -i bandit17.chiave bandit17@bandit.labs.overthewire.org -p 2220
	(su bandit17)
	cat /etc/bandit_pass/bandit17
	return:
		(password)
# Password sbloccata:
	pWXMAZoxGC8JmDMfmT5MGEsobMM3vnj2