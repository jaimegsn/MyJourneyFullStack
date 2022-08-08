#### Modificador Final em tipo por Referência

O modificador Final ele transforma as variáveis do tipos referência  em constantes ou seja elas ficam imutáveis, porém os atributos do objeto instanciado na variável ainda pode mudar, o que não muda é o objeto atrelado a variável.

Uma boa prática para declarar uma constante é nomeá-la em capslock e se for nome composto utilizar   o ´ _ ´ para separar 

EX:

```java
// Exemplo em tipo referência

import revisao.Revisao;
public class App {
    public static void main(String[] args) {
        final Pessoa p = new Pessoa();  // Definição da constante do tipo referência
	    p.nome = "Jaime"; // Mudar os atributos ainda pode        
	    p = new Pessoa(); // O que não é permitido é mudar o valor da variavel
    }
}
```