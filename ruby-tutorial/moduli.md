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
		