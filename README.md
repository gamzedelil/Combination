# Combination
package combination;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {
	
		Scanner input = new Scanner(System.in);
		
		int n, r, result=1, result2=1, result3=1;
		System.out.println("Enter n:");
		n = input.nextInt();
		
		System.out.println("Enter r:");
	    r = input.nextInt();
	    result = 1;
	    
	    // calculating n!
	    for (int i = 1; i <= n; i++) {
            result *= i;
        }
	    
	    // calculating r!
	    for (int j = 1; j <= r; j++) {
            result2 *= j;
        }
	    
	    //calculating n-r!
	    int k = n-r;
	    for (int a = 1; a <=k ; a++) {
            result3 *= a;
        }
	    
	    int C = result / (result2 * result3);

        System.out.println("C(" + n + "," + r + ") = " + C);	    	
	}
}
