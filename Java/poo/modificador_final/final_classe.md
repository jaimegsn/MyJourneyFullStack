#### Modificador Final em Classes

O modificador final quando está sendo colocado juntamente com classes  está ligado diretamente a herança pois ao colocarmos o modificador na classe, queremos que essa classe não seja estendida, ou seja, não se torne uma super classe ou classe pai.

EX:

```java
// Classe com o modificador final :
public final class Carro {
    private String modelo;
    private String cor;
}

//Classe Ferrari
public class Ferrari extends Carro { // Apresentará erro pois a classe carro não pode ser estendida
    
}
```