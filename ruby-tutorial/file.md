# LEGGERE UN FILE         
      
Per leggere e visualizzare un file direttamente da linea di comando 
si utilizza il comando rb = File.open("es1.txt").readlines, che 
apre il file, lo visualizza nel terminale su una o più righe.
Di seguito, con il comando “puts rb”, nella linea di comando, 
stampa  tutto il contenuto del file come se venisse aperto con
l’editor (ovviamente il file che viene visualizzato sul terminale 
è di sola lettura).        
       
	>> rb = File.open("es1.rb").readlines       
	=> (testo completo del programma che è stato richiamato				
	>> puts rb     				
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
        
Un altro modo per leggere un file è con il comando “File.new” che 
darà  la possibilità di accedere al file ma in più permette di
specificare se il file possa essere di sola lettura, scrittura 
o entrambi. In seguito viene generato un ciclo che legge il file
una riga per volta e la inserisce in un array. Una volta finita
l’operazione è obbligatorio chiudere il file.      
		   
	>> f = File.new("es1.rb", "r")     
	=> # File:es1.rb    
	>> testo = [ ]     
	=> [ ]    
	>> while (riga = f.gets)     
	>> testo << riga     
	>> end    
	=> nil    
	>> f.clone    
	=> nil     
	>> num_righe = testo.length    
	=> 17     
	>> 0.upto num_righe - 1 do |n|    
	?> puts "#"{n}- #{testo[n]}     
	>> end    
