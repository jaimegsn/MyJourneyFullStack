#### Exemplo Dentro da Classe

Criamos o enum dentro da propria classe cliente e criamos um atributo do tipo enum dentro da classe:

```java
package devdojo;

public class Cliente {
    private String nome;
    private TipoCliente tipo; // AQUI a criação do atributo do tipo enum (TipoCliente)

    public enum TipoCliente { // AQUI a criação do enum
        PESSOA_JURIDIA,
        PESSOA_FISICA
    }

    public Cliente(String nome, TipoCliente tipo) {
        this.nome = nome;
        this.tipo = tipo;
    }
}
```

Classe main:

```java
public class Main {
    public static void main(String[] args) {
        Cliente cliente1 = new Cliente("Jaime", Cliente.TipoCliente.PESSOA_FISICA);
        Cliente cliente2 = new Cliente("Allan Jesus", Cliente.TipoCliente.PESSOA_JURIDIA);
        Cliente cliente3 = new Cliente("Neymar", Cliente.TipoCliente.PESSOA_FISICA);
    }
}
```