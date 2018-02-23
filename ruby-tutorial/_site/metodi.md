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

























 