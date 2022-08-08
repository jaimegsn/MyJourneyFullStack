#### Exemplo Classe

Criação da classe abstrata:

```java
public abstract class Funcionario {
    protected String nome;
    protected double salario;

    public Funcionario(String nome, double salario) {
        this.nome = nome;
        this.salario = salario;
    }

}
```

Classe Desenvolvedor que irá herdar funcionário:

```java
public class Desenvolvedor extends Funcionario {

    public Desenvolvedor(String nome, double salario) {
        super(nome, salario);
    }

    @Override
    public String toString() {
        return "Desenvolvedor []";
    }

}
```