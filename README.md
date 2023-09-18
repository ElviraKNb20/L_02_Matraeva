# L_02_Matraeva
import java.util.Scanner;

public class FindIncreasingNumber {
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введiть кiлькiсть чисел (n): ");
        int n = scanner.nextInt();
        int foundNumber = -1;
        for (int i = 0; i < n; i++) {
            System.out.print("Введiть числo: ");
            int number = scanner.nextInt();
            if (isIncreasing(number)){
                foundNumber = number;
                break;
            }
        }
        if (foundNumber != -1){
            System.out.println("Перше число, цифри в якому йдуть у строгому порядку зростання: " + foundNumber);
        }
        else {
            System.out.println("Не знайдено жодного числа з цифрами в строгому порядку зростання.");
        }
        scanner.close();
        }
        //Функція для перевірки, чи цифри в числі йдуть в строгому порядку зростання
    public static boolean isIncreasing (int number){
        String numStr = Integer.toString(number);
        for (int i = 0; i < numStr.length() - 1; i++){
            if (numStr.charAt(i) >= numStr.charAt(i+1)){
                return false;
            }
        }
        return true;
    }
    }
