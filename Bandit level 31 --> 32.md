# Comandi usati:
	rm -rf
	cd
	cat
	ls
	git add
	git commit -m
	git push
# Procedura:
	rm -rf repo
	git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-
	git/repo
	return.
		(oggetti copiati)
	
	cd repo
	ls -la
	return:
		totale 8  
		drwxr-xr-x. 1 nicola nicola  46 14 ago 16.43 .  
		drwx------. 1 nicola nicola 580 14 ago 16.43 ..  
		drwxr-xr-x. 1 nicola nicola 122 14 ago 16.43 .git  
		-rw-r--r--. 1 nicola nicola   6 14 ago 16.43 .gitignore  
		-rw-r--r--. 1 nicola nicola 147 14 ago 16.43 README.md
	
	cat .gitignore
	return:
		*.txt   (dice di ignorare qualsiasi file con l'estensione .txt)
	
	rm .gitignore
	cat README.md
	return:
		This time your task is to push a file to the remote repository.  
		
		Details:  
		File name: key.txt  
		Content: 'May I come in?'  
		Branch: master
	
	nano key.txt
		May I come in?
	
	git add key.txt   (o git add -f key.txt se non si vuole rimuovere .gitignore)
	git commit -m "Push key.txt"
	git push origin master
	return:
		Well done!
		(password)
# Password sbloccata:
	pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT