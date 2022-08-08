#### Múltiplas interfaces

É possível implementar mais de uma interface em uma classe:

Interface 1 DataLoader :

```java
public interface DataLoader {
    void load();
}
```

Interface 2 DataRemover:

```java
public interface DataRemover {
    void remove();
}
```

Classe que implementou as 2 interfaces:

```java
public class DatabaseLoader implements DataLoader, DataRemover {

    @Override // Método sobrescrito do DataLoader
    public void load() {
        System.out.println("Dados carregados");
    }

    @Override // Método sobrescrito do DataRemover
    public void remove() {
        System.out.println("Dados Removidos");
    }

}
```