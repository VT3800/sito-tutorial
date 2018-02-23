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
		
