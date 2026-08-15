# Comandi usati:
	ssh
	echo
	nc -lvp
	&
# Procedura:
	ssh bandit20@bandit.labs.overthewire.org -p 2220
	echo 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA | nc -lvp 37658 &
	
	(dà la password a nc tramite echo che di norma scrive a schermo, mentre nc si
	mette in ascolto, con anche -v per verbose, scrivere più informazioni, e -p
	per specificare la porta, utile per essere sicuri anche se spesso non serve;
	con & metti il processo in background per fare altro nel mentre)
	 
	./suconnect 37658
	return:
		(password)
# Password sbloccata:
	bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY