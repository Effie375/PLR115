[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Feffie375.github.io%2FTPTE-AEGEAN&count_bg=%23E3802B&title_bg=%2307359E&icon=internetarchive.svg&icon_color=%23E7E7E7&title=%CE%A0%CF%81%CE%BF%CE%B2%CE%BF%CE%BB%CE%AD%CF%82&edge_flat=false)](https://hits.seeyoufarm.com)

# Eργαστήριο 2

## Άσκηση 1

Δημιουργήστε πρόγραμμα το οποίο θα διαβάζει διάφορα προϊόντα και θα σταματάει όταν δοθεί ως απάντηση οποιοσδήποτε ακέραιος αριθμός διάφορος του 1. Το κάθε προϊόν θα έχει τρεις ιδιότητες (όνομα, τιμή και βαθμός  αξιολόγησης) και θα το συγκρίνουμε με το καλύτερο προϊόν για να δούμε αν είναι καλύτερο. Για να βρούμε αν ένα προϊόν είναι καλύτερο από άλλο  συγκρίνουμε τις βαθμολογίες τους οι οποίες είναι η διαίρεση του βαθμού αξιολόγησης διά της τιμής. Αν η βαθμολόγια είναι μεγαλύτερη τότε αλλάζουμε τις τιμές των ιδιοτήτων του καλύτερου προϊόντος με το τρέχων προϊόν. Στο τέλος εκτυπώνουμε τις ιδιότητες του καλύτερου προϊόντος.

```Java
import java.util.Scanner; 
 
class Main { 
  public static void main(String[] args) { 
     
    Scanner keyboard = new Scanner(System.in); 
     
    String bestName = ""; 
    double bestPrice = 1; 
    float bestScore = 0; 
     
    boolean more = true; 
     
    while(more) { 
     
      System.out.println("Dose onoma proiontos: "); 
      String nextName = keyboard.nextLine(); 
      System.out.println("Dose timi proiontos: "); 
      double nextPrice = keyboard.nextDouble(); 
      System.out.println("Dose vathmologia proiontos: "); 
      float nextScore = keyboard.nextFloat(); 
     
      if (nextScore/nextPrice > bestScore/bestPrice) { 
      bestName = nextName; 
      bestPrice = nextPrice; 
      bestScore = nextScore; 
      } 
 
      System.out.println("Perissotera proionta? 1:YES, 2:NO"); 
      int answer = keyboard.nextInt(); 
      if (answer != 1) 
        more = false; 
      keyboard.nextLine(); 
    } 
 
    System.out.println("To onoma tou kaliterou proiontos einai: " + bestName); 
    System.out.println("H timi tou kaliterou proiontos einai: " + bestPrice); 
    System.out.println("H vathmologia tou kaliterou proiontos einai: " + bestScore); 
  } 
} 
```
