[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Feffie375.github.io%2FTPTE-AEGEAN&count_bg=%23E3802B&title_bg=%2307359E&icon=internetarchive.svg&icon_color=%23E7E7E7&title=%CE%A0%CF%81%CE%BF%CE%B2%CE%BF%CE%BB%CE%AD%CF%82&edge_flat=false)](https://hits.seeyoufarm.com)

# Eργαστήριο 3

## Άσκηση 1

Η κλίμακα που χρησιμοποιείται για τους τυφώνες, τους κατατάσσει σε 5 κατηγορίες σύμφωνα με τον παρακάτω πίνακα:

|Κατηγορία|Ταχύτητα Ανέμου(σε κόμβους)|
|:-:|:-:|
|1|64 – 83|
|2|84 – 96|
|3|97 – 113|
|4|114 – 134|
|5|>=135|

Ένας κόμβος ισούται με 1.85 χλμ./ώρα. Να γραφεί πρόγραμμα, το οποίο:

- θα διαβάζει την ταχύτητα του ανέμου.
- θα εμφανίζει τη λέξη «KATHGORIA» και δίπλα σε ποια κατηγορία ανήκει.
- θα μετατρέπει τους κόμβους σε χλμ./ώρα και θα εμφανίζει «XLM/ORA» και δίπλα πόσα χλμ./ώρα είναι ο άνεμος.

```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        float komvoi;
        float xlm;

        Scanner keyboard = new Scanner(System.in);

        System.out.println("Dwse taxitita anemou se komvous: ");
        komvoi = keyboard.nextFloat();

        if(komvoi >= 64 && komvoi <= 83) {
            System.out.println("KATHGORIA 1");
        }
        else if(komvoi >= 84 && komvoi <= 96) {
            System.out.println("KATHGORIA 2");
        }
        else if(komvoi >= 97 && komvoi <= 113) {
            System.out.println("KATHGORIA 3");	
        }
        else if(komvoi >= 114 && komvoi <= 134) {
            System.out.println("KATHGORIA 4");	
        }
        else if(komvoi >= 135) {
            System.out.println("KATHGORIA 5");	
        }
        System.out.println("XLM/ORA: "+ komvoi * 1.85);
    }
}

```

## Άσκηση 2

Να γραφεί πρόγραμμα, το οποίο:

- Θα διαβάζει μία θερμοκρασία σε βαθμούς Φαρενάιτ (F).
- Θα μετατρέπει τη θερμοκρασία σε βαθμούς Κελσίου (C) σύμφωνα με τον παρακάτω τύπο: C=(F-32)/(212-32)*100.
- Θα εμφανίζει το μήνυμα «BATHMOI KELSIOU» και δίπλα την θερμοκρασία σε βαθμούς Κελσίου.
- Θα εμφανίζει το μήνυμα «ZESTH» αν η θερμοκρασία είναι πάνω από 20 βαθμούς Κελσίου, «KRYO» αν η θερμοκρασία είναι μεταξύ 0 και 20 βαθμούς Κελσίου και «PAGONIA» αν είναι κάτω από 0 βαθμούς Κελσίου.
	
```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        float F;

        Scanner keyboard = new Scanner(System.in);

        System.out.println("Dwse thermokrasia(F): ");
        F = keyboard.nextFloat();

        float C = (F-32)/(212-32)*100;

        System.out.printf("BATHMOI KELSIOU %f \n", C);

        if(C >= 0 && C <= 20) {
            System.out.println("KRYO");
        }
        else if(C > 20) {
            System.out.println("ZESTH");
        }
        else{
            System.out.println("PAGWNIA");
        }
    }
}

```
