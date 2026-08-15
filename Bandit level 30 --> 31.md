# Comandi usati:
	rm -rf
	cd
	cat
	ls
	git log --all --oneline --graph
	git tag
# Procedura:
	rm -rf repo
	git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-
	git/repo
	return:
		(oggetti copiati)
	
	cd repo
	cat README.md
	return:
		just an epmty file... muahahaha
	
	git log --all --oneline --graph
	return:
		* 929c564 (HEAD -> master, origin/master, origin/HEAD) initial commit of 
		README.md
	
	git tag
	return:
		secret
	
	git show secret
	return:
		(password)
# Password sbloccata:
	82NkymblpGBYmIXG6ZQ8YldBYstHpfUf