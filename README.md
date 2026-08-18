import java.util.Scanner;

class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String pass, again;

        while (true) {
            System.out.print("Enter password: ");
            pass = sc.nextLine();

            if (pass.length() < 8) {
                System.out.println("Need 8 characters.");
            } else if (!pass.matches(".*[A-Z].*")) {
                System.out.println("Need 1 capital letter.");
            } else if (!pass.matches(".*[0-9].*")) {
                System.out.println("Need 1 number.");
            } else {
                System.out.print("Re-enter password: ");
                again = sc.nextLine();

                if (pass.equals(again)) {
                    System.out.println("Password Accepted!");
                    break;
                } else {
                    System.out.println("Passwords do not match.");
                }
            }
        }
    }
}
