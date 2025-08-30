// COMPOUND INTEREST CALCULATOR

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double principal;
        double rate;
        int term;
        double amount;
        double interestComponent;

        System.out.print("Enter the amount of Principal INR : ");
        principal= scanner.nextDouble();

        System.out.print("Enter the rate of interest (in %) : ");
        rate= scanner.nextDouble()/100 ;

        System.out.print("Enter the term (in years) : ");
        term= scanner.nextInt();

        amount= principal * Math.pow(1 + rate, term);

        interestComponent= amount-principal;

        System.out.printf("The amount after %d year/s is INR %.2f, at your bank account and your interest component meanwhile is INR %.2f.", term, amount, interestComponent);

        scanner.close();
    }
}
