#### Sobrecarga de Métodos

O tipo de polimorfismo de Sobrecarga permite a existência de vários métodos de mesmo nome, porém com assinaturas levemente diferentes, ou seja, variando no número e tipo de argumentos.

```java
public class Cachorro {
    public void perseguirMoto(String latir) {
        System.out.println(latir);
    }

    public void perseguirMoto(String latir, String correr) {
        System.out.println(latir);
        System.out.println(correr);
    }

    public void perseguirMoto(int velocidade) {
        System.out.println("auauauau");
        System.out.println("Correndo a " + velocidade + " P/Minuto");
    }
}
```

Existe também uma boa prática com sobrecarga quando queremos adicionar um novo parâmetro a um método sem quebrar o código, visto que esse método já foi aplicado diversas vezes no nosso código, e adição avulsa de um novo parâmetro irá acarretar em erros de sintaxe, podemos fazer uma sobrecarga para solucionar isso:

```java
public class Cachorro {
    private int patas;
    private String nome;
    private String raca;

    public void init(String nome, String raca) {
        this.nome = nome;
        this.raca = raca;
    }

    // Então queremos adicionar um novo parâmetro patas no método acima por n
    // motivos, fazemos:
    public void init(String nome, String raca, int patas) {
        init(nome, raca);
        this.patas = patas;
    }
}
```