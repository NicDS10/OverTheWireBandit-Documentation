# Comandi usati:
	ssh
	cd
	cat
	ls
	file
	tar
	gzip
	bzip2
	mkdir
	mktemp
	xxd
	mv
	cp
# Procedura:
	ssh bandit12@bandit.labs.overthewire.org -p 2220
	ls
	return:
		data.txt
	cd tmp
	mkdir cartella
	cd cartella
	cp /home/bandit12/data.txt . (ovvero quì)
	file data.txt
	return:
		ASCII text
	xxd -r data.txt > binario1
	file binario1
	return:
		gzip compressed data
	mv binario1 data.gz
	gzip -d data.gz | file data
	return:
		bzip2 compressed data
	mv data data.bz2
	bzip2 -d data.bz2 | file data
	return:
		gzip compressed data
	mv data data.gz
	gzip -d data.gz | file data
	return:
		POSIX tar archive (GNU)
	mv data data.tar
	tar -xvf data.tar
	return:
		data5.bin
	file data5.bin
	return:
		POSIX tar archive (GNU)
	tar -xvf data5.bin
	return:
		data6.bin
	tar -xvf data6.bin
	return:
		data8.bin
	file data8.bin
	return:
		gzip compressed data
	mc data8.bin data8.gz
	gzip -d data8.gz | dile data8
	return:
		ASCII text
	cat data8
	return:
	The password is (password)
# Password sbloccata:
	qQYQiHOBPR8zR61qxYqX45quvihF2uzk