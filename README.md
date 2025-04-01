# cs50
 solve an actual problem, that you impact your community, or that you change the world.
import java.io.*;
import java.util.*;

public class TaskMaster {
    private static final String FILENAME = "tasks.txt";
    private static List<String> tasks = new ArrayList<>();

    public static void main(String[] args) {
        loadTasks();
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("\n=== TaskMaster ===");
            System.out.println("1. Add Task");
            System.out.println("2. View Tasks");
            System.out.println("3. Delete Task");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");

            int choice = scanner.nextInt();
            scanner.nextLine(); // Consume newline

            switch (choice) {
                case 1:
                    addTask(scanner);
                    break;
                case 2:
                    viewTasks();
                    break;
                case 3:
                    deleteTask(scanner);
                    break;
                case 4:
                    saveTasks();
                    System.out.println("Tasks saved. Good
