#### Default ( Métodos Concretos)

Ao criar uma interface e implementa-la na classe temos que implementar de fato ela sobrescrevendo os métodos, se não o Java aponta erro de código.

Então em um projeto grande se formos adicionar um novo método na interface teremos que ir manualmente em todas as classes que ele está implementado e sobrescrever esse método novo, se não apresentará erros.

Então para solucionar isso existem os métodos Default em interfaces que podem ou não ser implementados de fato.

Os métodos Default devem ter um corpo

EX:

```java
public interface DataRemover {

    default void printData() { // Opcional implementação
        System.out.println("Dados");
    };

    void remove(); // Implementação obrigatória
}
```

EX implementando em outra classe  outra classe:

```java
public class DatabaseLoader implements DataRemover {

    @Override // Método sobrescrito do DataRemover
    public void remove() {
        System.out.println("Dados Removidos");
    }

}
```