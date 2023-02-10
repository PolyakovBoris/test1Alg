import java.util.Scanner;

public class Main {
    public static void main(String[] args) {


// 1.Составить алгоритм: если введенное число больше 7, то вывести “Привет”

        Scanner scanner = new Scanner(System.in);
        System.out.println("Введите число -> ");
        if (scanner.hasNextInt()) {
            if (scanner.nextInt() > 7) {
                System.out.println("Привет");
            }
        } else {
            System.out.println("вы ввели не число ");
        }


//  2.	Составить алгоритм: если введенное имя совпадает с Вячеслав, то вывести “Привет, Вячеслав”, если нет, то вывести "Нет такого имени"

        System.out.println("Введите имя -> ");
        String userInput = scanner.next();
        if (userInput.trim().equals("Вячеслав")) {
            System.out.println("Привет, " + userInput);
        } else {
            System.out.println("Нет такого имени");
        }

//  3.	Составить алгоритм: на входе есть числовой массив, необходимо вывести элементы массива кратные 3

        System.out.println("\nСколько чисел будете вводить? ");
        String arrLen = scanner.next();
        int[] arr = new int[Integer.parseInt(arrLen)];
        System.out.println("Введите числа через ENTER -> ");
        for (int i = 0; i < arr.length; i++) {
            String userInput2 = scanner.next();
            arr[i] = Integer.parseInt(userInput2);
        }
        System.out.println("Получен числовой массив -> ");
        for (int elem : arr) {
            System.out.print(elem + " ");
        }
        System.out.println("\nЭлементы массива кратные 3 -> ");
        for (int item : arr) {
            if (item % 3 == 0) {
                System.out.print(item + " ");
            }
        }
        scanner.close();
    }
}

// 4. Дана скобочная последовательность: [ ( (()) () (()) ]]
- Можно ли считать эту последовательность правильной? - нет
- Если ответ на предыдущий вопрос “нет” - то что необходимо в ней изменить, чтоб она стала правильной? – необходимо предпоследнюю ] заменить на )
