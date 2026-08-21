# Comandi usati:
	ssh
	find
# Procedura:
	ssh bandit6@bandit.labs.overthewire.org -p 2220
	find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
	return:
		/var/lib/dpkg/info/bandit7.password
	cat /var/lib/dpkg/info/bandit7.password
	return:
		password
# Password sbloccata:
	Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3