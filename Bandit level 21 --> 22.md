# Comandi usati:
	ssh
	cron
	ls -la
	cat
	cd
# Procedura:
	ssh bandit21@bandit.labs.overthewire.org -p 2220
	cd /etc/cron.d
	cat cronjob_bandit22
	return:
		@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null  
		* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
		(le * indicano la frequenza con cui cron le esegue, bandit22 i permessi 
		di chi sta usando e poi il file che esegue)
	
	cat /usr/bin/cronjob_bandit22.sh
	return:
		chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv  
		cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
		(apre il file con la password e la mette in quel file)
		
	cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
	return:
		(password)
# Password sbloccata:
	RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz