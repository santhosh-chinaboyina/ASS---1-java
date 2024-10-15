# java-assignment-mid-1
import java.io.*;
import java.util.Scanner;

 class Calculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double num1, num2;
        char operator;

        System.out.print("Enter first number: ");
        num1 = scanner.nextDouble();

        System.out.print("Enter second number: ");
        num2 = scanner.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        operator = scanner.next().charAt(0);

        double result;

        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println("Result: " + result);
                break;
            case '-':
                result = num1 - num2;
                System.out.println("Result: " + result);
                break;
            case '*':
                result = num1 * num2;
                System.out.println("Result: " + result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + result);
                } else {
                    System.out.println("Error: Division by zero");
                }
                break;
            default:
                System.out.println("Error: Invalid operator");
                break;
        }

        scanner.close();
    }
}
