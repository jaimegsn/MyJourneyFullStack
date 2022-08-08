#### Exemplo

```java
//Interface Data Loader

public interface DataLoader {
    void imprimirOla(); // Está implicito que é um méotodo abstrato
    public abstract void imprimirFlamengo();//É redundante colocar o modificador de abstato
}
```

```java
//Classe DatabaseLoader

public class DatabaseLoader implements DataLoader {

    @Override
    public void imprimirOla() {
        System.out.println("Olá");
    }

    @Override
    public void imprimirFlamengo() {
        System.out.println("Flamengo");
    }

}

```