#### Métodos Abstratos

Métodos abstratos são métodos que não possui corpo, ele apenas existe para ser sobrescrito por uma sub classe.

Classe Abstrata com o Método abstrato :

```java
public abstract class Funcionario {
    protected String nome;
    protected double salario;

    public Funcionario(String nome, double salario) {
        this.nome = nome;
        this.salario = salario;
    }

    public abstract double CalculaBonus(); // Criamos o método abstrato
}
```

Implementando ele na sub classe Desenvolvedor:

```java
public class Desenvolvedor extends Funcionario {

    public Desenvolvedor(String nome, double salario) {
        super(nome, salario);
    }

    @Override
    public double CalculaBonus() {  // Sobrescrita Aqui
        return super.salario + (super.salario * 0.1);
    }
}
```