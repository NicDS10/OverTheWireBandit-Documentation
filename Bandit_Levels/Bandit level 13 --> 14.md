# Comandi usati:
	ssh -i
	ls
	cat
	scp -P
# Procedura:
	(da terminale privato, sennò non si hanno i permessi per creare file e si 
	dovrebbe andare su tmp, ma anche lì non si può fare chmod 600; inoltre, non 
	ci si può collegare tramite localhost all'interno dei server bandit)
	
	ssh bandit13@bandit.labs.overthewire.org -p 2220
	scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private 
	chmod 600 sshkey.private
	ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
	(entri sul server bandit come bandit14)
	cat /etc/bandit_pass/bandit14
	return:
		(password)
# Password sbloccata:
	aaWecNkG4FhxJQxz07uiwzVP6bJiYS65