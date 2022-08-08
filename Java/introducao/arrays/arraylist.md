#### Array List

O array list ele permite que o tamanho do array cresça dinamicamente dentro do tempo de execução 

Lembre-se de que o arraylist não aceita tipos primitivos(int,double,float), apenas tipos por referência (Integer,String,Double).

Para criamor um arraylist precisamos importa o list e o arryalist e depois seguir o codigo:

```java
import java.util.ArrayList;
import java.util.List;

public class App {
    public static void main(String[] args) {
        List<String> textos = new ArrayList<>();
        List<Cadeira> cadeira = new ArrayList<>();

        textos.add("Texto1"); // Adicionar elemento no arraylist
        System.out.println(textos.get(0));  // Exibir o elemento da posição 0 

        for (String t : textos) {  // Percorrer o ArrayList com ForEach
            System.out.println(t);
        }

    }
}
```