# RUBY (parte 1)<h1>      

## INDICE <h2>  
	1. Introduzione;  
	2. Editor e console;  
	3. Operazioni;  
		- matematiche;  
		- confronto;  
	4. Stringhe;  
	5. Conversioni;  
	6. Array;  
	7. Variabili;  
	8. Range;   
	9. Dizionari o hash;  
    10. Blocchi;  
    11. Controlli di flusso;  
    12. Cicli;  
    13. Metodi;  
		 - definizione di un metodo;   
		 - tipi di metodi;  
    14. Moduli;  
    15. Classi;  
    16. Sottoclassi;  
    17. Leggere un file;  
    18. Programmi.  
 
## INTRODUZIONE <h2>    
     
Ruby è un linguaggio orientato agli oggetti ed è interpretato(il codice sorgente viene tradotto in maniera istantanea e vengono eseguite le istruzioni così come 
indicare nel codice sorgente, senza bisogna di compilatori).    
Il suo principale obbiettivo è permette al programmatore di usufruire di un linguaggio semplice che gli permetta di essere veloce e produttivo. 

## EDITOR <h2>     
     
Ruby è multipiattaforma e quindi disponibile per Linux, Windows, Mac OS e altri sistemi operativi minori. 
Non esiste un vero e proprio editor per Ruby ma nella maggior parte dei casi si tratta di editor già esistenti (in genere di Java) che sono dotati di pulgin per Ruby.    
Quindi, in linea di massima, si può utilizzare qualsiasi editor di testo, ad esempio Emacs, Vi o Notepad.  
Esistono tuttavia ambienti di sviluppo che integrano un supporto a Ruby più completo come NetBeans, IntelliJ IDEA e Eclipse.

## CONSOLE <h2>      
     
La console di Ruby viene denominata irb(Interactive Ruby Shell), e per usufruirne basta digitare il comando “irb”, sulla Shell della linea di comando.       
       
**irb(main):001:0>**   
   
Se si vuole utilizzare un prompt più breve, basta digitare il comando “irb --prompt simple”    
**>>**   
         
		   
# OPERAZIONI <h1>

#### Matematiche <h4>

Con Ruby si possono eseguire operazioni matematiche. Qui di seguito possiamo vedere alcuni esempi:

      
	>> 5+6 (+ addizione)           
	=> 11            
	>> 7-2 (- sottrazione)          
	=> 5     		   
	>> 3*8 (* moltiplicazione)          
	=> 24     	     
	>> 9/3 (/ divisione)         
	=> 3       	  
	>> 3**2 (** elevazione a potenza)         
	=> 9     	       
	>> 4%2 (% modulo)        
	=> 0      	      	
	>> 7/2.0  (operazione con float)         
	=> 3.5      	    
	
	
#### Confronto <h4>

Con Ruby si possono usare gli operatori di confronto per comparare dei
valori utilizzando i seguenti simboli: <, >, ==, !=, <=, >=. 
Questi simboli possono essere usati anche con le stringhe in base all’ordine alfabetico:
‘a’ > ‘b’ => false oppure ‘b’ > ‘a’ => true, perché ‘b’ venendo dopo nell’alfabeto è maggiore
di ‘a’(le maiuscole vengono prima delle minuscole);      
     
\>> 'a' > 'b'    
=> false     
\>> 'B' < 'A'    
=> false     
     
     	 
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
            
	\>> 'Pippo è andato dall\'altra parte'            
	=> "Pippo è andato dall'altra parte"             
	\>> "Pippo è andato dall'altra parte"        
	=> "Pippo è andato dall'altra parte"       
         
		 
# CONVERSIONI <h1>

In Ruby è possibile convertire le stringhe, i numeri e gli array, con i seguenti comandi:     
	1. **To_s**(to string), converte i valori in stringhe;    
	2. **To_i** (to int), converte i valori in interi;    
	3. **To_a** (to array), converte i valori in array;     
>
\>> 456.to_s.reverse.to_i    
=> 654     

In questo caso, l’utente ha convertito il numero intero 456, in stringa per poterlo invertire, 
e successivamente lo ha riconvertito in intero.		
         

# ARRAY <h1>       

Sono liste, contrassegnate dalle parentesi quadre ([ ]), che possono essere composte da numeri, stringhe ecc.
Per creare un array vuoto si scrivono le parentesi quadre, senza elementi al loro interno; invece per creare un array di elementi si scrive per esempio: [num1,num2,num3]
Con gli array si possono utilizzare i seguenti comandi:        
      
1. **[ ].max**, prende il numero più grande contenuto nell’array;       
	\>> [1,2,3].max    
	=> 3     
2. **[ ].min**, prende il numero più piccolo contenuto nella lista;     
	\>> [1,2,3].min     
	=> 1    
3. **[ ].sort**, mette in ordine crescente l’array;         
	\>> [3,1,2].sort   
	=> [1,2,3]    
4. **[ ].last**, restituisce l’ultimo numero della lista;      
	\>> [1,2,3].last          
	=> 3           
5. **[ ].reverse**, inverte l’array;           
	\>> [1,2,3].reverse         
	=> [3,2,1]    
6. **[ ].push(num)**, aumenta la lunghezza dell’array, aggiungendo il numero inserito nelle parentesi;         
	\>> [1,2,3].push(4)       
	=> [1,2,3,4]  
7. **[ ].pop**, restituisce l’ultimo valore che abbiamo inserito nell’array.             
	\>> [1,2,3].pop            
	=> 3       		

Gli array possono contenere anche delle stringhe. Qui di seguito si possono vedere alcuni esempi:    
         
\>> "Ciao".chars.to_a    
=> ["C", "i", "a", "o"]       
\>> "Ciao".chars.to_a.reverse       
=> ["o", "a", "i", "C"]     
       
Nel primo caso la stringa viene convertita in un array,mentre nel secondo caso viene trasformata e invertita.        
        
		
# VARIABILI 
		
Sono dei contenitori identificati da un nome univoco, di un qualsiasi valore, sia esso un numero o una stringa. 
Le variabili vengono definite da un tipo e un nome (definito identificatore). Per assegnare un valore ad una variabile viene utilizzato il simbolo dell’uguale (=). Le variabili vengono distinte in: locali, globali, di istanza, di classe e costanti. 
		
* **variabili locali**, per convenzione, devono iniziare con una lettera minuscola o con il carattere underscore( _ ). Sono definite nella funzione (o nel blocco) che le usa; nascono quando la funzione entra in esecuzione e muoiono al termine dell’esecuzione della funzione.  
* **variabili globali**, vengono contrassegnate con il segno <b> $ </b>. Valgono dal punto di definizione fino alla fine del file. Lo spazio viene allocato ed inizializzato di default a zero, a meno che sia diversamente inizializzato dal programmatore. 
* **variabili di istanza**, vengono distinte con il segno <b> @ </b>. È una variabile associata a una classe di oggetti che rappresenta un elemento dell'informazione contenuta nell'oggetto stesso. 
* **variabili di classe**, vengono identificate con <b> due </b> segni @. Una variabile di classe corrisponde al concetto di variabili statiche in altri linguaggi come Java e PHP. È dunque una variabile che appartiene alla classe il cui valore è comune a tutte le istanze della classe stessa. 
* **costanti**, vengono definite con la prima lettera o con i caratteri che compongono il suo nome maiuscoli. Identifica una porzione di memoria il cui valore non varia nel corso dell'esecuzione di un programma.

>			
Qui di seguito si può osservare come si assegna un valore a una variabile e come si può richiamare.    
	\>> contenitore = [3,4,5,6,7,8,9]     
	=> [3,4,5,6,7,8,9]     
	\>> contenitore     
	=> [3,4,5,6,7,8,9]      
        
# RANGE <h1>    

In Ruby esiste anche il comando per indicare un range di valori e questo viene identificato con due punti (..).      
Qui di seguito si possono osservare alcuni esempi:       
               
\>> (1..5).each {|a| print "#{a}, "}        
1,2,3,4,5, => 1..5       
\>> ("bad".."bag").each {|a| print "#{a}, "}      
bad, bae, baf, bag, => "bad".."bag"         
     
	 
Nel primo caso viene stampato un range di numeri da 1 a 5, mentre nel secondo caso si marca un range di stringhe da “bad” a “bag”.       
Essendo le prime lettere delle stringhe uguali, viene analizzata solo l’ultima lettera e quindi il range si basa dalla lettera “d” alla “g” seguendo l’ordine alfabetico.
        

# DIZIONARI o HASH
		
Per creare un dizionario/hash si utilizzano le parentesi graffe ({ }). 
Negli hash l’indice può essere di qualsiasi tipo, rispetto all’array, e può essere una stringa o un’ espressione regolare; per salvare un valore in un hash è necessario specificare sia l’indice, che il  valore associato ad esso.    
        
	>> nome = Hash.new(0)     
	=> {}     
	>> 5.times{print 'ciao '}     
	ciao ciao ciao ciao ciao => 5     
        			
Nel primo caso viene creato un nuovo dizionario vuoto, mentre nel secondo viene ripetuto il contenuto del dizionario per 5 volte, a seconda del numero indicato dall’utente.       
*Esempio:*    
      
Qui è stato creato un hash vuoto.   
              
	>> cibo = {}          
	=> {}              
		
Gli hash di seguito indicati contengono  un insieme di key(chiave) => value(valore). Al loro interno le chiavi sono rappresentate dalle pietanze mentre i valori dall’indice di gradimento.      
         	
	>> cibo [" Carciofi "] = : non_buono     
	=> : non_buono      
	>> cibo [" Salsiccia "] = : molto_buono     
	=> : molto_buono       
	>> cibo [" Pajata "] = : non_so     
	=> : non_so      
	>> cibo [" Mozzarella "] = : buono      
	=> : buono     
	>> cibo [" Aragosta "] = : ottimo     
	=> : ottimo    
        
Come indicato nel caso sottostante, se richiamato, il dizionario cibo mostra a video il suo contenuto.        			
         
	>> cibo     
	=> {" Carciofi " => : non_buono, " Salsiccia " => : molto_buono ... }     
        
Di seguito viene creato un hash per memorizzare l’indice di gradimento e successivamente viene riempito con le recensioni.    
        
	>> recensioni = Hash.new(0)     
	=> {}     
	>> food.values.each {|voto| recensioni [voto]+= 1}      
         
Una volta richiamato, mostra a video i risultati        			
       
	>> recensioni      
	=> {: non_buono => 2, : molto_buono => 4, : non_so => 1,...}      		
	

