#### Exemplo Arquivo Separado

```java

// Classe do tipo ENUM com 2 opções:
public enum TipoCliente {
    PESSOA_JURIDIA, // Opção 1
    PESSOA_FISICA  // Opção 2
//Note que não é necessário falar nenhum tipo primitivo ou de referencia pois esses dados são do Tipo:  TipoCliente
}
```

Agora segue o mesmo processo de relação por associação, criamos um atributo do TipoCliente dentro da classe de interesse que no nosso caso é cliente:

```java
public class Cliente {
    private String nome;
    private TipoCliente tipo;  // AQUI

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
        Cliente cliente1  = new Cliente("Jaime",TipoCliente.PESSOA_FISICA);
        Cliente cliente2  = new Cliente("Allan Jesus",TipoCliente.PESSOA_JURIDIA);
        Cliente cliente3  = new Cliente("Neymar",TipoCliente.PESSOA_FISICA);
    }
}
```