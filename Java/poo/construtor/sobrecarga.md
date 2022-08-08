#### Sobrecarga de Construtor

Existe uma boa prática em Java para quando se quer adicionar parâmetros ao construtor, sem quebrar o código, muito utilizado em códigos grandes com centenas de classes, mas primeiro vamos ver o PROBLEMA:

Adicionando um novo parâmetro( COR ) ao construtor

```java
// Classe Fogão:
package introducao;
public class Fogao {
    private int bocas = 0;
    private boolean gas = true;
    private String cor = null;

    public Fogao(int bocas, boolean gas, String cor){ // Novo parâmetro COR
        this.bocas = bocas;  this.gas = gas; this.cor = cor;
    }

}

// Classe Main:
package introducao;
public class DevDojo {
    public static void main(String[] args) {
        Fogao f = new Fogao(4,true); //  Aqui apresentará um problema visto que o construtor pede 3 parâmetros
    }
}
```

Com esse problema é possível perceber que a adição avulsa de um novo parâmetro reflete em uma manutenção mais árdua e complicada, pois temos que atualizar todas as instâncias daquele objeto adicionando o novo parâmetro.

Então para isso temos a sobrecarga de construtor, onde reescrevemos o mesmo construtor com o novo parâmetro.

Então vamos rescrever a classe Fogão com a Solução:

```java
// Classe Fogão
package introducao;
public class Fogao {
    private int bocas = 0;
    private boolean gas = true;
    private String cor = null;

    public Fogao(int bocas, boolean gas){
        this.bocas = bocas; this.gas = gas;
    }

    public Fogao(int bocas, boolean gas, String cor){ // Sobrecarga com novo parâmetro
        this.bocas = bocas; this.gas = gas; this.cor = cor;
				//ou
				this(bocas, gas); // Deve estar na 1° linha do novo construtor
        this.cor = cor;
    }

}
```