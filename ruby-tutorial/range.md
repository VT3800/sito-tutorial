# RANGE <h1>    

In Ruby esiste anche il comando per indicare un range di valori e questo viene identificato con due punti (..).      
Qui di seguito si possono osservare alcuni esempi:       
               
\>> (1..5).each {|a| print "#{a}, "}        
1,2,3,4,5, => 1..5       
\>> ("bad".."bag").each {|a| print "#{a}, "}      
bad, bae, baf, bag, => "bad".."bag"         
     
	 
Nel primo caso viene stampato un range di numeri da 1 a 5, mentre nel secondo caso si marca un range di stringhe da “bad” a “bag”.       
Essendo le prime lettere delle stringhe uguali, viene analizzata solo l’ultima lettera e quindi il range si basa dalla lettera “d” alla “g” seguendo l’ordine alfabetico.
