# Comandi usati:
	ssh
	ls
	diff
# Procedura:
	ssh bandit17@bandit.labs.overthewire.org -p 2220
	ls
	return:
		passwords.old passwords.new
	diff passwords.old passwords.new
	return:
		42c42 (la riga diversa)
		< icUh23IUytZLIYhcCaXL18agiSIqymBc (linea originale)
		---  	
		> OQxXZjELndr90zuhOTDYBEomI0SZITXI (linea modificata e password)
# Password sbloccata:
	OQxXZjELndr90zuhOTDYBEomI0SZITXI