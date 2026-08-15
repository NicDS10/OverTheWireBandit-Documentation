# Comandi usati:
	rm -rf
	git clone
	cd
	cat
	ls
	git log --all --oneline --graph
	git show
# Procedura:
	rm -rf repo
	git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-
	git/repo
	return:
		(oggetti clonati)
	git log --all --oneline --graph
	return:
		* 0bf8160 (origin/dev) add data needed for development  
		* 1b95ced add gif2ascii  
		| * a0e9e9c (origin/sploits-dev) add some silly exploit, just for shit 
		| and giggles  
		|/     
		* b607fba (HEAD -> master, origin/master, origin/HEAD) fix username  
		* 84c16f8 initial commit of README.md
	
	git show 0bf8160
	(il primo commit, che poi è stato nascosto per un merge con un altro branch)
	return:
		## credentials  
		- username: bandit30  
		
		-- password: <no passwords in production!>  
		+- password: (password)
# Password sbloccata:
	jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX