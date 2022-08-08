#### Construtores, exemplo em Arquivos Separados

Aqui cada opção/valor da enumeração terá seu parâmetro de construtor :

```java
public enum TipoCliente {
    PESSOA_JURIDIA(1),  // Opção enum com parâmetro
    PESSOA_FISICA(2);  // Opção enum com parâmetro

    public final int VALOR; // Criação da constante que irá armazenar o parâmetro

    TipoCliente(int valor) { // Construtor
        this.VALOR = valor;  // Atribuição do valor passado pelo parâmetro
    }
}
```

Classe Cliente:

```java
public class Cliente {
    private String nome;
    private TipoCliente tipo;

    public Cliente(String nome, TipoCliente tipo) {
        this.nome = nome;
        this.tipo = tipo;
    }

    @Override
    public String toString() {
        return "Cliente [nome=" + nome + ", tipo=" + tipo + ", Valor Tipo=" + tipo.VALOR + "]";
    }

}
```

Classe Main:

```java
public class Main {
    public static void main(String[] args) {
        Cliente cliente1 = new Cliente("Jaime", TipoCliente.PESSOA_FISICA);
        Cliente cliente2 = new Cliente("Allan Jesus", TipoCliente.PESSOA_JURIDIA);
        Cliente cliente3 = new Cliente("Neymar", TipoCliente.PESSOA_FISICA);

        System.out.println(cliente1);
    }
}
```