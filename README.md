# square-and-triangle

import java.util.Scanner;

public class bentuk {

		public static void triangle(int rows){
			int spaces = rows - 1;
			
			for(int i = 1; i<=rows; i++) {
				for(int j = 1; j<=spaces; j++) {
					System.out.print(" ");
				}
				spaces--;
				
				for(int j = 1 ; j<=2*i-1; j++) {
					System.out.print("*");
				}
				System.out.println();
			}
		}

		public static void square(int rows){
			for(int i = 1 ;i<=rows ; i++) {
				for(int j = 1; j<=rows ;j++) {
					if(i!=1 && i!=rows && j!=1 && j!=rows) {
						System.out.print(" ");
					} else {
						System.out.print("*");
					}
					
				}
				System.out.println();
			}
		}
		
		public static void main(String[] args) {
			Scanner input = new Scanner(System.in);
			System.out.print("Shape: ");
			String string = input.nextLine();
			
			if(string.equals("square")) {
				System.out.print("Size: ");
				int size = input.nextInt();
				square(size);
			} else if(string.equals("triangle")) {
				System.out.print("Size: ");
				int size = input.nextInt();
				triangle(size);
			} else {
				System.out.println("not valid");
			}
			
			input.close();
		}
	
}
