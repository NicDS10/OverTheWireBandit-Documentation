# Comandi usati:
	ssh
	ncat --ssl
	openssl s_client
# Procedura:
	ssh bandit15@bandit.labs.overthewire.org -p 2220
	ncat --ssl localhost 30001 < /etc/bandit_pass/bandit15
	return:
		Correct!
		(password)
# Password sbloccata:
	kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V