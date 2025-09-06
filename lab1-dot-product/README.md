import java.util.Random; // tool used to generate random numbers

public class Lab1DotProduct { // The main class of file
    public static void main(String[] args) { // Start of program, void of comments
        int[] a = new int[5]; 
        int[] b = new int[5];
        
    //two interger arrays with n =5
        Random rand = new Random(); // object to generate intergers
        for (int i = 0; i <5; i++){
            a[i] = rand.nextInt(18)+1;
            b[i] = rand.nextInt(18)+1;
        // random number between 1 and 18
       
        int dotProduct = 0; 
        // initialize variable to store dot product
        
        
        for (int i=0; i < 5; i++) { //
            dotProduct += a[i] * b[i];
            //
            System.println(a[i] + " * " + b[i] + " = " + (a[i] * b[i]));
        }
                System.out.println("Dot prodduct is: " + dotProduct);   
                    
        }        
    }
}
