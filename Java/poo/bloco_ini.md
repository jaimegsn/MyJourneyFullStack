#### Blocos de Inicialização

São usado em casos muito particulares quando queremos que recursos estejam disponíveis antes que a classe faça o seu trabalho, esse recursos podem ser variáveis, bibliotecas, tratamento de exceção…

São usado, por exemplo, para carregar biblioteca nativas. No drivers JDBC são usados para registrar a classe no DriverManager.

O bloco de inicialização static é executado assim que a classe é carregada e um não static é executado antes do construtor.

Outra diferença entre o bloco de inicialização static para o não static é que o não static é executada toda vez em que o objeto é instanciado, se tem 3 objetos ele é executado 3 vezes enquanto que o static como é atrelado a classe  e não depende de objeto ele só é iniciado 1 vez não importando a quantidade de objetos.

Ex:

```java
package introducao;

public class Fogao {
    private int bocas = 0;
    private boolean gas = true;

    {
        System.out.println(" Aqui é o Bloco de inicialização");
        this.gas = false;
    }
    
    static
    {
        System.out.println(" Aqui é o Bloco de inicialização static");
    }

    public Fogao(int bocas, boolean gas) {
        this.bocas = bocas;
        this.gas = gas;
    }

}
```