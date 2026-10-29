import java.util.Random;
import java.util.Scanner;

public class GuessNumberGame {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        boolean playAgain;

        do {
            int secret = random.nextInt(11); // 0..10
            boolean guessed = false;

            System.out.println("Я загадал число от 0 до 10. У вас 3 попытки.");

            for (int attempt = 1; attempt <= 3; attempt++) {
                System.out.print("Попытка " + attempt + "/3: ");
                int guess = scanner.nextInt();

                if (guess == secret) {
                    System.out.println("Вы угадали! Это число " + secret);
                    guessed = true;
                    break;
                } else if (guess < secret) {
                    System.out.println("Загаданное число БОЛЬШЕ.");
                } else {
                    System.out.println("Загаданное число МЕНЬШЕ.");
                }
            }

            if (!guessed) {
                System.out.println("Вы проиграли. Было число " + secret);
            }

            System.out.print("Повторить игру ещё раз? 1 - да / 0 - нет: ");
            playAgain = scanner.nextInt() == 1;

        } while (playAgain);

        scanner.close();
    }
}
