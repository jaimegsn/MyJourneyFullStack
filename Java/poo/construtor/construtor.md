#### Construtor

Serve para inicializar recurso ao instanciar um objeto, um exemplo seria atribuir valores aos atributos  e não possui nenhum retorno

Criando o método construtor

```java
public class Cadeira {
    private String cor;
    private String material;

    public Cadeira(String c, String m){ // Construtor
        this.cor=c;
        this.material=m;
    }
}
```

Atribuindo os valores ao instanciar um objeto:

```java
public class App {
    public static void main(String[] args) {
        Cadeira c  = new Cadeira("Cor verde","Material Madeira");
    }
}
```

[Sobrecarga de Construtor](sobrecarga.md)