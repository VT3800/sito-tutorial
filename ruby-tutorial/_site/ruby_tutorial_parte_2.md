# RUBY (parte 2)<h1>       
        
# BLOCCHI <h1>        

Gestiscono i dettagli all’interno del metodo, l’istallazione, la rimozione e gli errori (non visibili all’utente).           
     
\>> food.values.each{|voto| recensioni[voto] += 1}      
       
In questo esempio, **|voto|** è la variabile di blocco, dove vengono contenuti tutti i valori di food, mentre **recensioni [voto] += 1** 
è il codice di blocco, dove vengono eseguiti. 
        
# CONROLLI DI FLUSSO 
     
I controlli di flusso in sostanza vengono rappresentati da IF, THEN, ELSE , UNLESS, ELSIF/ ELSE IF e CASE.
Qui di seguito osserviamo:     
     
* nel primo caso il passaggio di una stringa e il controllo con if-then/else,
	  se la stringa è piena o vuota; se la sequenza di caratteri contiene qualcosa 
	  restituirà un messaggio altrimenti ne restituirà un altro per dirci che non 
	  contiene niente.    
		\>> string = 'a string'    
		=> "a string"    
		\>> if string == " " then    
		\?> "La stringa non contiene niente"    
		\>> else    
		\?> "La stringa è piena"      
		\>> end     
		=> "La stringa è piena"      
         
* nel secondo caso, verrà utilizzato il comando if not e unless 
	 (che hanno lo stessa funzione), per controllare se la variabile ‘x’ 
	  contiene o no qualcosa.     
		\>> x = 'un oggetto'     
		=> "un oggetto"    
		\>> puts "x non è vuoto" if not x.empty?      
		x non è vuoto    
		=> nil    
		\>> puts "x non è vuoto" unless x.empty?    
		x non è vuoto    
		=> nil
       		
* Se ci sono più condizioni, solitamente si tende ad utilizzare il comando 
	  “else if” oppure “elsif” per risparmiare caratteri. Prima dell’ ’end’ 
	  possiamo mettere l’ “else” che verrà eseguito se in nessuno dei precedenti 
	  casi viene soddisfatta la condizione richiesta.    
         
* Quando ci sono molti casi, ce la possibilità di utilizzare il comando 
	  “case” che prende come argomento il dato che si vuole controllare e ad 
	  ogni caso bisogna scrivere “when” seguito dall’espressione che può 
	  risultare e il codice a lui sottoscritto.     
	        
	  puts 'Dimmi la tua età: '    
	  eta = gets.to_i      
       
	  case eta     
		when 6     
			puts 'Stai facendo la prima elementare'      
		when 7            
		    puts 'Stai facendo la seconda elementare'       
		when 8      
			puts 'Stai facendo la terza elementare'     
		when 9       
			puts 'Stai facendo la quarta elementare'         
		when 10        
			puts 'Stai facendo la quinta elementare'       
		else      
		    if eta > 10      
				puts 'Probabilmente sei alle medie o alle superiori'      
			else       
				puts 'Non sei mai andato a scuola'        
		end            
	  end 	
     
# CICLI <h1>    

Esistono differenti modi per ripetere un blocco di codice. Quelli analizzati sono: WHILE, UNTIL e FOR.                
1. **while...end**, ripete il blocco di codice finché la condizione è vera;    
2. **until...end**, se la condizione è falsa replica una determinata azione;    
3. **for...in...end**, per ogni elemento all’interno di un insieme di valori esegue un’ operazione.   
	      
	\>> numeri = [1,2,3,4,5,6,7,8]   
	=> [1,2,3,4,5,6,7,8]   
	\>> for numero in numeri      
	\>>puts numero      
	?> end     
	1     
	2     
	3    
	4     
	5      
	6     
	7      
	8      
	=> [1,2,3,4,5,6,7,8]    
        
# METODI <h1>      

#### COME SI DEFINISCE UN METODO? <h4> 
  
Per creare un metodo si utilizza il comando DEF e per terminarlo si usa END.      
\>> def metodo     
\>> end    
=> nil     
     
Una volta creato un metodo, si richiama scrivendo il nome e l’argomento (se definito nel metodo), sulla riga di comando.     
     
\>> metodo      
=> nil     
      
I metodi presenti all’interno di una classe (che si vedrà in seguito) sono solitamente **pubblici**, e cioè possono essere utilizzati al di fuori della 
classe, in qualsiasi parte del codice. Se si vuole richiamare un metodo solo all’interno della sua classe è necessario dichiararlo come **privato**, 
mettendo la parola “private” prima di definire il metodo. Per richiamare il metodo privato è necessario creare un altro metodo all’interno del 
programma che permetta di richiamare il metodo e così da poterlo utilizzare.

*Esempio:*    
          
	class Human    
		attr_accessor :name, :age      
      		
*#metodo pubblico*     
              
		def dimmi_di_te                  
			puts "Ciao, sono #{@name} e ho #{@age} anni."    
		end      
     
*#metodo pubblico che ci permette di richiamare il metodo privato*      
           
		def confessa    
			dimmi_un_segreto        
		end          
		      
		private      
		def dimmi_un_segreto           
			puts "Non sono umano, sono un robot"     
		end      
	end    

*#creo un nuovo oggetto di tipo Human*      
        
h = Human.new   
   
*#diamo un valore ai parametri da passare alle funzioni*     
           
h.name = "Marvin"   
h.age = 31   
   
*#richiamo i due metodi*      
          
h.dimmi_di_te   
h.confessa   


#### TIPI DI METODI <h4>
In questo linguaggio di programmazione sono presenti differenti metodi;    
qui di seguito ne vengono indicati alcuni:        
	1. **EACH**, metodo che accetta un blocco di codice e lo esegue per ogni elemento della lista. I bit tra Do e END sono un unico blocco;      
	2. **EXIST? (‘miofile.txt’)**, controlla che il file esista;   
	3. **FILE? (‘miofile.txt’)**, controlla se un file è un documento;   
	4. **DIRECTORY?(‘miadirectory’)**, controlla se un file è una cartella (directory);    
	5. **FTYPE (‘miofile.txt’)**, controlla che tipo di file è, per esempio se è un documento o una directory;   
	6. **SIZE (‘miofile.txt’)**, controlla quanto è grande e la quantità di spazio che occupa sul disco;    
	7. **JOIN (‘cartella1’,’cartella2’,’miofile.txt’)**, costruisce un percorso di file concatenando due o più stringhe;     
	8. **BASENAME (‘/cartella1/cartella2/miofile.txt’)**, restituisce il nome del mio file;    
	9. **DIRNAME (‘/cartella1/cartella2/miofile.txt’)**, riporta il percorso delle directory senza il nome del file;       
   10. **EXTNAME (‘miofile.txt’)**, scrive sulla linea di comando l’estensione del nome del file, cioè il testo dopo il punto, comprendendolo;    
   11. **MAP**, invoca il codice di blocco indicato una volta per ogni elemento self e crea un nuovo array contenente i valori restituiti dal blocco;        
   12. **SELECT**, è simile a map ma restituisce solo gli elementi che corrispondono alla condizione.       
         
# MODULI <h1>            
        
I moduli, in Ruby, sono simili alle classi, ma a differenza di quest’ultime,
non possono avere istanze, non hanno sottoclassi e sono definiti da 
MODULE…END. Per poter essere eseguiti all’interno del programma i 
moduli devono essere sempre inclusi, altrimenti il programma non 
riconosce i metodi definiti all’interno del modulo.       
       
	module Pippo      
		def dice(cosa)      
			puts "pippo dice: "+ cosa      
		end             
	end      
        
	include Pippo      
	dice('ciao')     	
      
I questo caso nel programma riportato sopra, viene mostrata la creazione 
del modulo Pippo e al suo interno viene inserito un metodo che stampa una 
stringa. Come argomento si può passare sia un numero che una stringa.
Dopo aver definito il modulo va incluso e successivamente viene richiamato 
il metodo “dice”  il cui argomento è una stringa. La stringa risultante 
sarà: “Pippo dice: ciao”.      
        
# CLASSI      
     
Una classe è una raccolta di metodi, il cui nome, per convenzione inizia 
con una lettera maiuscola. Per inizializzare una classe è necessario 
scrivere “CLASS” e per terminarla si scrive “END”.  Quando si vuole 
creare un nuovo oggetto (un’istanza) della classe che si va a definire
bisogna inserire il comando “nome_classe.new”.      
       
Un’ istanza è un particolare oggetto di una determinata classe. 
Ogni istanza è separata dalle altre, ma condivide le sue caratteristiche 
generali con gli altri oggetti della stessa classe.       
			
Per definire un oggetto è quindi necessario individuare:       
* le sue caratteristiche (attributi);
* le azioni che compie e/o subisce (metodi).
       
Per accedere agli attributi  di una classe, ci sono tre possibilità:     
* **attr_reader**, serve per accedere a un attributo in sola lettura;  
* **attr_writer**, si utilizza per accedere a un attributo in sola scrittura;
* **attr_accessor**, viene usato per accedere in scrittura e lettura.
        
Nel programma sottostante, viene creata la classe Persona, e al suo 
interno si vanno a definire due metodi “inizialize” e “goodbye”. 
Successivamente,  dopo aver creato la classe, vengono istanziati 
due oggetti di tipo Persona (p1,p2) che richiameranno i due metodi.     
      
*Esempio:*    
      
	class Persona      
		def inizialize    
			puts "Ciao !"    
		end    
       		
		def goodbye    
			puts "Arrivederci !"     
		end    
	end     
		
*#creiamo due oggetti della classe Persona*      
		p1= Persona.new    
		p2= Persona.new     
      
*#richiamo il metodo creato dalla classe*      
		puts p1.inizialize    
		puts p2.goodbye       
       
# SOTTOCLASSI <h1>          
      
Per definire una sottoclasse in Ruby viene utilizzato il 
simbolo "<”: es. Palindromo < String, in questo caso “Palindromo”
è sottoclasse di “String”. La sottoclasse eredita tutti i metodi
pubblici della superclasse (classe da cui eredita).      
      
*Esempio:*  	
            
		class Palindromo < String          
			def palindrome?              
				self == self.reverse           
			end     
		end      
		parola = Palindromo.new("Anna")      
		puts parola.palindrome?     
     
In questo esempio viene creata la sottoclasse “Palindromo”, che ha 
al suo interno il metodo che verifica se la parola inserita dall’utente
è palindroma o no. Dopo aver definito la classe, viene creato un 
oggetto di tipo Palindromo, dove vengono inseriti la stringa con 
la parola che si vuole verificare. Successivamente viene richiamato 
il metodo che dirà se la parola è palindroma o meno.

# SOTTOCLASSI <h1>          
      
Per definire una sottoclasse in Ruby viene utilizzato il 
simbolo "<”: es. Palindromo < String, in questo caso “Palindromo”
è sottoclasse di “String”. La sottoclasse eredita tutti i metodi
pubblici della superclasse (classe da cui eredita).      
      
*Esempio:*  	
            
		class Palindromo < String          
			def palindrome?              
				self == self.reverse           
			end     
		end      
		parola = Palindromo.new("Anna")      
		puts parola.palindrome?     
     
In questo esempio viene creata la sottoclasse “Palindromo”, che ha 
al suo interno il metodo che verifica se la parola inserita dall’utente
è palindroma o no. Dopo aver definito la classe, viene creato un 
oggetto di tipo Palindromo, dove vengono inseriti la stringa con 
la parola che si vuole verificare. Successivamente viene richiamato 
il metodo che dirà se la parola è palindroma o meno.