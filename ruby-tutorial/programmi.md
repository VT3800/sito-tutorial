# PROGRAMMI  <h1>           
        
Questo programma serve per creare una tabella contenente le tabelline dei
numeri da 1 a 10:      
       
	numeri = [1,2,3,4,5,6,7,8,9,10]       
         
	for n in numeri           
		riga = ' '     
		for moltiplicatore in numeri     
			valore = n * moltiplicatore     
			if valore < 10     
				separatore = ' '      
			else       
				separatore = ' '    
			end          
			riga = riga + valore.to_s + separatore      
		end     
		puts riga    
	end    
       
	   
Nel programma seguente viene creata una calcolatrice che esegue le 4 operazioni 
matematiche in base alla scelta dell’utente:      
       
*#programma che esegue le 4 operazioni*     
	      
		puts "Che operazione vuoi svolgere: "     
		puts "1. Addizione"     
		puts "2. Sottrazione"    
		puts "3. Moltiplicazione"     
		puts "4. Divisione"      
      
*#prelevo il numero inserito dall'utente*     
	     
		num = gets.chomp.to_i       
        
*#eseguo il controllo*
    	
		while num < 1 || num > 4     
			puts "il numero inserito non è corretto"     
			puts "Inserisci un numero tra 1 e 4"    
			num = gets..chomp.to_i      
		end       
         
		case(num)        
			when 1				
				puts "inserisci il primo numero      
				x = gets.to_i       			
				puts "inserisci il secondo numero      
				y = gets.to_i     
				risultato = x + y       				
				*trasforma il risultato in stringa*            
				puts  "Risulta: " + risultato.to_s       
        				
			when 2        			
				puts "inserisci il primo numero"       
				x = gets.to_i       
				puts "inserisci il secondo numero"     
				y = gets.to_i      
				risultato = x - y      
				puts  "Risulta: " + risultato.to_s       
        				
			when 3           
				puts "inserisci il primo numero"       
				x = gets.to_i       
				puts "inserisci il secondo numero"           
				y = gets.to_i      
 				risultato = x * y      
				puts "Risulta: " + risultato.to_s        
          
			when 4      
				puts "inserisci il primo numero"     
				x = gets.to_i     
				puts "inserisci il secondo numero"      
				y = gets.to_i      
				risultato = x / y       
				puts  "Risulta: " + risultato.to_s        
       
			else       
				puts " "      
			end      
		end     
       
Qui di seguito si può osservare un programma che contiene un dizionario; quando viene eseguito, 
vengono fornite chiave e valore, che sono contenuti nel dizionario:      
       
	dizionario = {'nome' => 'pippo', 'cognome' => 'pluto'}     
      
	dizionario.each do |chiave,valore| *prende chiave e valore*     
		puts 'chiave '+ chiave *stampa il valore che abbiamo assegnato alla chiave*     
		puts 'valore '+ valore     
	end     
