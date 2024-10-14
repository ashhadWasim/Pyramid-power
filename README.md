# Pyramid-power
With user-provided numbers, This program creates a reverse-pyramid pattern and also calculates exponents.
This Java code was created and worked on Eclipse:



import java.util.Scanner;

public class Star_Power {
	
	static Scanner console = new Scanner (System.in);

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		//Problem 1
		System.out.println("Enter the number of lines: ");
		int num = console.nextInt();
		printStarPattern(num);
		//////////////////////////////////////////////////////
		System.out.println();
		//Problem 2
		System.out.println("Enter a number: ");	
		int num2 = console.nextInt();
		System.out.println("To what power? ");	
		int pow = console.nextInt();
		System.out.println("Value of " + num2 + " to the " + pow + " power is: " + power(num2,pow));
		System.out.println();

	}
	
	static double power(int number, int powerOf) {
		if(powerOf == 1) {
			return number;
		}//end if
		return power(number,--powerOf)*number;
		
	}//end power

	private static void printStarPattern(int num) {
		
		if(num == 0) {
			return;	
			}//end if
		else if(num < 0) {
			System.out.println("Number MUST be positive");
		} //end else if
		else {
			
			for(int i=0; i<num; i++) {
			System.out.print("*");
			}//end for loop(1st half)
	
			System.out.println();
			printStarPattern(--num);
			
			}//end else
		
		
			for(int i=0; i<=num; i++) {
			System.out.print("*");
			}//end for loop(2nd half)
				
			System.out.println();
	
	}//end printStarPattern

	

}
