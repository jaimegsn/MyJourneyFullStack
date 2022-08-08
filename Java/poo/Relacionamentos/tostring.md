#### Método toString (Sobrescrita)

Toda as classes no Java são filhas da classe object (java.lang.Object)

dentro da classe object existe um método chamado toString, onde ele retorna em String os dados daquela classe, por padrão é retornado o nome da classe e o hashcode do objeto.

Porém é uma prática comum sobrescrever esse método dentro das classes, visto que todas as classes são filhos dela.

E dentro da  sobrescrita é comum colocar os dados daquela classe como por exemplo, valores de atributos, mas isso fica a critério de quem está programando como ele é um método que já existe então basta depois da sobrescrita chama-lo normalmente quando o objeto estiver instanciado.

EX:

```java
// Classe com o ToString:
package revisao;
public class Revisao {
    private int teste = 5;

    @Override
    public String toString() {
        return "O valor da variável teste é: " + teste;
    }
}

// Classe Main:
import revisao.Revisao;

public class App {
    public static void main(String[] args) {
        Revisao r = new Revisao();
        System.out.println(r.toString());
    }
}
```