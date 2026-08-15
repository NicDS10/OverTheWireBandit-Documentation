# Comandi usati:
	ssh
	ls
	cat --
	\
# Procedura:
	ssh bandit2@bandit.labs.overthewire.org -p 2220
	ls
	return:
		--spaces in this filename--
	cat --spaces in this filename--
	return:
		 unexpected argument '--spaces' found  
		tip: to pass '--spaces' as a value, use '-- --spaces'  
		Usage: cat [OPTION]... [FILE]...  
		For more information, try '--help'.
	cat -- --spaces in this filename--
	return:
		cat: --spaces: No such file or directory  
		cat: in: No such file or directory  
		cat: this: No such file or directory  
		cat: filename--: No such file or directory
	cat -- --spaces\ in\ this\ filename--
	return:
		password
# Password sbloccata:
	7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME