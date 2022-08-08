#### Programação Orientada a Interface

Na programação orientada a interface nós podemos criar uma variável do tipo interface a atribuir a ela objetos das classes que implementaram essa interface EX:

Interface:

```java
public interface Repositorio {
    public abstract void salvar();
}
```

Classes implementando a interface:

```java
public class RepositorioArquivo implements Repositorio {
    @Override
    public void salvar() {
        System.out.println("Salvando um arquivo");
        
    }
}

public class RepositorioDados implements Repositorio {
    @Override
    public void salvar() {
        System.out.println("Salvando um dado");
        
    }
}
```

Main:

```java
public class Main {
    public static void main(String[] args) {
        Repositorio repositorio = new RepositorioArquivo();
        repositorio.salvar();
				// Trocando para outro objeto que também tem a interface implementada
        repositorio = new RepositorioDados();
        repositorio.salvar();
    }
}
```

Porém como vimos em upcasting. Só é possivel acessar os métodos/atributos da interface repositorio.