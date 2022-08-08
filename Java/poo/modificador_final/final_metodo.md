#### Modificador Final em Método

O modificador final quando está sendo colocado juntamente com métodos  está ligado diretamente a herança, pois ao colocarmos o modificador no método queremos que esse método não seja sobrescrito.

EX:

```java
// Classe com o modificador final no método :
public class Carro {
    public final void imprimir() {
        System.out.println("Impressão da classe carro");
    }
}

//Classe Ferrari
public class Ferrari extends Carro {

    @Override
    public void imprimir() {  // Apresentará erro pois esse método não pder ser sobrescrito
        System.out.println("Impressão Ferrari");
    }
}
```