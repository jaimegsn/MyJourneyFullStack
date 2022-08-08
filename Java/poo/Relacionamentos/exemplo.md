#### Exemplo

Superclasse/Classe Pai:

```java
package heranca;

public class Pessoa {
    private String nome = null;
    private String cpf = null;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getCpf() {
        return cpf;
    }

    public void setCpf(String cpf) {
        this.cpf = cpf;
    }
```

Subclasses/ Classes filho:

```java
//Classe Funcionário
package heranca;

public class Funcionario extends Pessoa {   // extends Pessoa significa que Funcionario ta herdando os métodos da classe Pessoa
    private double Salario = 0;

    public double getSalario() {
        return Salario;
    }

    public void setSalario(double salario) {
        Salario = salario;
    }
}
```

Classe Main:

```java
package heranca;

public class Main {

    public static void main(String[] args) {

        Pessoa pessoa = new Pessoa();
        pessoa.setNome("Jaime");
        pessoa.setCpf("2131231");

        Funcionario func1 = new Funcionario();
        func1.setNome("Pedro"); // Método herdado de pessoa
        System.out.println(func1.getNome());

    }
}
```