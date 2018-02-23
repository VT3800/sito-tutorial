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