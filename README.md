# Progetto-Lista-Attivit-
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class TaskList {
    public static void main(String[] args) {
        List<String> tasks = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("1. Nuova attività");
            System.out.println("2. Visualizza attività");
            System.out.println("3. Esci dalla lista");

            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.println("Inserisci una nuova attività: ");
                    String task = scanner.next();
                    tasks.add(task);
                    break;
                case 2:
                    System.out.println("Elenco delle attività:");
                    for (int i = 0; i < tasks.size(); i++) {
                        System.out.println((i + 1) + ". " + tasks.get(i));
                    }
                    break;
                case 3:
                    System.out.println("Arrivederci!");
                    System.exit(0);
            }
        }
    }
}

