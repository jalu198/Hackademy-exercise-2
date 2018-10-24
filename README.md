# Hackademy-exercise-2
This algorithm solves the next problem: By listing the first six prime numbers: 2, 3, 5, 7, 11, and 13, we can see that the 6th prime is 13. What is the 10 001st prime number?

package numerosprimos;
public class NumerosPrimos {
    public static void main(String[] args) {
        int n1 = 10001, n2 = 2;
        ArrayList<Integer> NumeroPrevio = new ArrayList<Integer>();
		    while (NumeroPrevio.size() < n1){			
			          boolean div = false;
 			          for (int numeroPrimo : NumeroPrevio){
                    if (n2 % numeroPrimo == 0 && numeroPrimo != n2){
				                div = true;
				                break; 
                    }
			          }
 			         if(!div){
				           if(!numeroPrevio.contains(n2))
                       numeroPrevio.add(n2);		
			         }
           n2++;		
	 	    }
 		    System.out.println("Lista de números primos: " + numeroPrevio);	
		    System.out.println("El " + n1 + "número primo es:" + numeroPrevio.get(numeroPrevio.size()-1));
		} 
}
