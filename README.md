# Implementing-Recursion-to-Provide-a-Sum

import java.util.Scanner;

public class RecursiveSum {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] numbers = new int[5];

        // Ask the user to enter five numbers
        System.out.println("Enter five numbers:");
        for (int i = 0; i < 5; i++) {
            numbers[i] = scanner.nextInt();
        }

        // Calculate the sum using recursion
        int sum = recursiveSum(numbers, 0);
        System.out.println("The sum of the entered numbers is: " + sum);
    }

    // Recursive method to calculate the sum
    public static int recursiveSum(int[] numbers, int index) {
        // Base case: if index is equal to the length of array, return 0
        if (index == numbers.length) {
            return 0;
        }
        // Recursive case: return the current number plus the sum of the rest
        return numbers[index] + recursiveSum(numbers, index + 1);
    }
}
}


