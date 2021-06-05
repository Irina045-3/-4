import java.util.Scanner;
import java.util.Random;
import java.lang.Math.*;

public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
		
		int n, m;
		System.out.print("n = ");
		n = sc.nextInt();
		System.out.print("m = ");
		m = sc.nextInt();
		
		int a[][] = new int[n][m];
		Random random = new Random();
		for(int i = 0; i < n; i++)
		    for(int j = 0; j < m; j++)
		        a[i][j] = random.nextInt(20);
		        
		 for(int i = 0; i < n; i++){
		    for(int j = 0; j < m; j++) System.out.print(a[i][j] + " ");       
		    System.out.println();
		 }
		
		int x;
		System.out.print("Enter number: ");
		x = sc.nextInt();
		sc.close();
		
		for(int i = 0; i < n; i++)
		    for(int j = 0; j < m; j++)
		        if(a[i][j] == x && Math.abs(i-j)%2 == 1){
		            System.out.println("a[" + i + ", " + j + "] = " + a[i][j]);
		        }
		
	}
}
