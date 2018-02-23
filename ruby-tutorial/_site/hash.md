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
	