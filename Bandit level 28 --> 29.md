# Comandi usati:
	rm
	git clone
	ssh
	cd
	cat
	git log
	git show
# Procedura:
	rm -rf repo (quella del livello precedente, sennò ha lo stesso nome)
	git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-
	git/repo
	return:
		(oggetti copiati)
	
	cd repo
	cat README.md
	return:
		# Bandit Notes  
		Some notes for level29 of bandit.
		
		## credentials  
		- username: bandit29  
		- password: xxxxxxxxxx
	
	git log README.md   (la storia dei commit)
	return:
		(fix info leak)
		(add missing data)
		(initial commit)
	
	git show 2678cfadd8f2a347bc23e1ea491f702e5b184709 
	(il commit 2 dove aggiungono dati)
	return:
		## credentials  
		- username: bandit29  
		
		-- password: <TBD>  
		+- password: (password)
# Password sbloccata:
	Em7eGtqaMySwNFjCpwzzHhLhospOcdt0