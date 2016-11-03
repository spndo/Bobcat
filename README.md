# Bobcat
A school project about renting a car
import java.util.Scanner;
public class Bobcar {
	public static void main (String[]args) {

		Scanner input = new Scanner(System.in);

		int days;
		double result = 0;
		double result2 = 0;
		double result3 = 0;
		double platinum = 0;

		System.out.println("Available cars: 1 for Economy, 2 for Compact, 3 for Standard ");
		System.out.println("Please choose the rental car: ");
		int car = input.nextInt();
		System.out.println("Please enter the number of rental day: ");
		days = input.nextInt();

		System.out.println("Club member?: 1 for yes, 0 for no: ");
		int member = input.nextInt();

		if (member == 1){
			System.out.println("Platinum Executive Package?: 1 for yes, 0 for no");
			platinum = input.nextDouble();
		}

		System.out.println("     ");


		if (car == 1){
			result = days * 25;
			System.out.println("Base: " + days + " days for a Economy @ $25 per day:" + "    " + "$" + result);

		} else if (car == 2){
			result = days * 55;
			System.out.println("Base: " + days + " days for a Compact @ $55 per day:" + "  " + "$" + result);


		} else if (car == 3){
			result = days * 100;
			System.out.println("Base: " + days + " days for a Standard @ $100 per day:" + "   " + "$" + result);
		}


		if ((member == 1) && (car ==1 )){
			if (days >= 5){
				result2 = (int)(days/5)*25;
				System.out.println ("Club Member Discount:" + "                      " + "-"+"$"+ result2);
			}else{
				System.out.println("CLub Member Discount:                       -$0");
			}
		}		
		if ((member == 1) && (car ==2 )){
			if (days >= 5){
				result2 = (int)(days/5)*55;
				System.out.println ("Club Member Discount:" + "   " + "-"+"$"+ result2);
			}else{
				System.out.println("Club Member Discount:                        -$0");
			}

		}
		if ((member == 1) && (car ==3 )){
			if (days >= 5){
				result2 = (int)(days/5)*100;
				System.out.println ("Club Member Discount:                         " + "-"+"$"+ result2);
			} else{
				System.out.println("Club Member Discount:                         -$0");
			}

		}


		if (member == 0){
			System.out.println("                    ");
		}

		if ((platinum == 1)&&(member == 1)){
			result3 = result * 0.2;
			System.out.println("Platinum Executive Package:                   " + "+"+ "$" + result3);
		}else 
			System.out.println("                ");

		System.out.println("    ");

		System.out.println("Total Estimate for Rental:                    " + "$" + (result - result2 + result3) ) ;








		input.close();}
}












