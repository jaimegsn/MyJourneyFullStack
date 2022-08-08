#### Interação com o usuário

Scanner

```java
import java.util.Scanner;
public class App {
    public static void main(String[] args) throws Exception {
        Scanner scanner = new Scanner(System.in);
        String txt = scanner.nextLine();
        System.out.println(txt);
    }
}
```

JOptionPane:

```java
import javax.swing.JOptionPane;
public class App {
    public static void main(String[] args) throws Exception {
        var txt = JOptionPane.showInputDialog("Insira um valor");
        JOptionPane.showMessageDialog(null,"Texto inserido:"+txt);
    }
}
```