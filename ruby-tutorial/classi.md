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