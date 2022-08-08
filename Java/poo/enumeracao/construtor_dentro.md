#### Construtores, exemplo dentro da classe

Aqui cada opção/valor da enumeração terá seu parâmetro de construtor :

```java
package devdojo;

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

    public enum TipoCliente { // Criação da classe de enumeração
        PESSOA_JURIDIA(1), // Opção da enumeração com o valor 1 como parâmetro
        PESSOA_FISICA(2);  // Opção da enumeração com o valor 1 como parâmetro

        public final int VALOR; // Constante que irá armazenar o valor do parâmetro

        TipoCliente(int valor) { //Construtor
            this.VALOR = valor;
        }
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