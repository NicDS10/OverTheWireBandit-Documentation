# Comandi usati:
	ssh
	cd
	file --
	cat --
# Procedura:
	ssh bandit4@bandit.labs.overthewire.org -p 2220
	cd inhere
	ls
	return:
		-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07
		-file08  -file09
	file -- -file00  -file01  -file02  -file03  -file04  -file05  -file06 
	-file07  -file08  -file09
	return:
		tutti i tipi di file, di cui 7 data, due criptati -file07 ASCII text
	cat -- -file07
	return:
		password
# Password sbloccata:
	6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG