# Comandi usati:
	ssh
	cd
	cat
	echo
# Procedura:
	ssh bandit22@bandit.labs.overthewire.org -p 2220
	cd /etc/cron.d
	cat cronjob_bandit23
	return:
		@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null  
		* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
	
	cat /usr/bin/cronjob_bandit23.sh
	return:
		myname=$(whoami)  
		mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)  
		(con $ sono variabili, quindi crea quel testo con bandit23, ne prende 
		l'hash col secondo comando e lascia solo la prima parte)
		
		echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
	
	echo I am user bandit23 | md5sum | cut -d ' ' -f 1  
	return:
		8ca319486bfbbc3663ea0fbe81326349
	cat /tmp/8ca319486bfbbc3663ea0fbe81326349
	return:
		(password)
# Password sbloccata:
	gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw