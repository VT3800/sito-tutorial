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
