# 3.1 Ασκήσεις

---

Εδώ θα βρείτε ένα σύνολο με ασκήσεις που βασίζονται στην ύλη του κεφαλαίου και αναδεικνύουν τις ιδιαιτερότητες του. Οι λύσεις των ασκήσεων βρίσκονται ακριβώς κάτω από κάθε εκφωνήση.

## 3.1.1 Άσκηση 1

---

Να γραφεί πρόγραμμα που θα διαβάζει το βαθμό ενός φοιτητή. Στη συνέχεια θα εμφανίζει Α αν ο βαθμός του φοιτητή είναι μεγαλύτερος ή ίσος με 90, Β αν ο βαθμός του φοιτητή είναι μεγαλύτερος ή ίσος με 70, C αν ο βαθμός του φοιτητή είναι μεγαλύτερος ή ίσος με 60, D αν ο βαθμός του φοιτητή είναι μεγαλύτερος ή ίσος με 50, και F σε διαφορετική περίπτωση.

```Java
import java.util.Scanner;

public class Main {
    public static void main (String[] args) {
        int number;
        
        System.out.print("Dose vathmo foititi: ");
        Scanner keyboard = new Scanner(System.in);
        
        number = keyboard.nextInt();
        
        if (number >= 90)
            System.out.println("A");
        else if (number >= 70)
            System.out.println("B");
        else if (number >= 60)
            System.out.println("C");
        else if (number >= 50)
            System.out.println("D");
        else
            System.out.println("F");
  }
}
```

## 3.1.2 Άσκηση 2

---

Να γραφεί πρόγραμμα το οποίο θα διαβάζει τον τελεστή (χαρακτήρα) της αριθμητικής πράξης (+ για πρόσθεση, - για αφαίρεση, * για πολλαπλασιασμό και / για διαίρεση. Στη συνέχεια θα διαβάζει δύο πραγματικούς αριθμούς. Με τη χρήση της εντολής switch θα υπολογίζει το αποτέλεσμα των τεσσάρων πράξεων και θα εκτυπώνει στην οθόνη το αποτέλεσμα ανάλογα με τον τελεστή που δόθηκε.

```Java
import java.util.Scanner;

    class Main {
    public static void main(String[] args) {
        
        char operator;
        Double number1, number2, result;
        
        Scanner keyboard = new Scanner(System.in);
        
        System.out.print("Enter operator (either +, -, * or /): ");
        operator = keyboard.next().charAt(0);
        
        System.out.print("Enter number1 and number2 respectively: ");
        
        number1 = keyboard.nextDouble();
        number2 = keyboard.nextDouble();
        
        switch (operator) {
            case '+':
                result = number1 + number2;
                System.out.print(number1 + "+" + number2 + " = " + result);
                break;
        case '-':
            result = number1 - number2;
            System.out.print(number1 + "-" + number2 + " = " + result);
            break;
        case '*':
            result = number1 * number2;
            System.out.print(number1 + "*" + number2 + " = " + result);
            break;
        case '/':
            result = number1 / number2;
            System.out.print(number1 + "/" + number2 + " = " + result);
            break;
        default:
            System.out.println("Invalid operator!");
            break;
            }
        }
}
```
