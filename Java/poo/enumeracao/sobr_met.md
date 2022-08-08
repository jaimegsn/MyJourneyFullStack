Classe enum TipoPagamento:

```java
public enum TipoPagamento{
    DEBITO{ // Se for Debito execute o Seguinte bloco de código:
        @Override
        public double desconto(double valor){ // Sobrescrita do Método desconto
            return valor-(valor*0.3);
        }
    },
    CREDITO{ // Se for Credito execute o Seguinte bloco de código:
        @Override 
        public double desconto(double valor){ // Sobrescrita do Método desconto
            return valor-(valor*0.1);
        }
    };

    public abstract double desconto(double valor);
}
```

Classe Main

```java
public class Main {
    public static void main(String[] args) {
        System.out.println(TipoPagamento.DEBITO.desconto(500));
    }
}
```