# STRINGHE 
Per scrivere una stringa vengono utilizzati i doppi apici (“ ”) o quelli singoli (‘ ’). Con le stringhe si possono utilizzare differenti comandi:
* **Downcase**, converte la stringa in minuscolo;
    >
	\>>'PIPPO'.downcase 
	>
	=> "pippo
* **Upcase**, converte la stringa in maiuscolo;
    >
	\>>'pippo'.upcase
	>
	=> "PIPPO" 
* **Capitalize**, restituisce una capia della stringa con il primo carattere maiuscolo;
    >
	\>> 'pippo'.capitalize 
	>
	=> "Pippo"
* **Swapcase**, restituisce una stringa con i caratteri invertiti, minuscole al posto di maiuscole e viceversa;
	>
	\>> 'PiPpO'.swapcase 
	>
	=> "pIpPo" 
* **Chop**, elimina l’ultimo carattere della stringa; <br>
	>
	\>> 'pippo'.chop 
	>
	=> 'pipp'		
* **Split(delimitatore)**, divide la stringa in sottostringhe in base al delimitatore passato come argomento;
	>
	\>> 'ciao mondo'.split 
	>
	=> ["ciao", "mondo"] 
	>
	\>> 'ciao mondo'.split('o') 
	>
	=> ["cia", "m", "nd"] 
* **“stringa1”+” stringa2”**, concatena le stringhe; 
	>
	\>> 'ciao ' + 'Pippo' 
	>
	=> "ciao Pippo" 
* **Reverse**, inverte la stringa(non utilizzabile con i numeri); 
	>
	\>> 'pippo'.reverse 
	>
	=> "oppip" 
* **Length**, mostra a video la lunghezza della stringa; 
	>
	\>> 'ciao Pippo'.length 
	>
	=> 10 
* **“stringa” x num**, replica la stringa per il numero di volte indicato da num; 
	>
	\>> 'pippo '*4 
	>
	=> "pippo pippo pippo pippo"
	>
* **\\**, è il carattere di escape, che trasforma il segno successivo in un carattere di tipo stringa e
  non viene visto come un simbolo di chiusura: es. ‘pippo è andato dall\’altra parte’, non visualizza errore se viene inserito un apice che funge da apostrofo; 
  Un altro utilizzo per non incappare in un errore è: “pippo  è andato dall’altra parte”, 
  dove vengono utilizzate le doppie virgolette in modo che se all’interno della frase viene messo un apice, quest’ultimo verrà visto come un carattere normale; 
	>
	\>> 'Pippo è andato dall\'altra parte' 
	>
	=> "Pippo è andato dall'altra parte" 
	>
	\>> "Pippo è andato dall'altra parte" 
	>
	=> "Pippo è andato dall'altra parte" 
	>
		
