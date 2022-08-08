#### Exemplo busca por atributos

Primeiramente devemos entender o método values( ), basicamente ele retorna todas as enumerações em um array.

Classe de enumeração TipoPagamento

```java
public enum TipoPagamento {
    DEBITO(1, "Débito"), // A Enumeração Débito
    CREDITO(2, "Crédito"); // A Enumeração Crédito

    public final int VALOR; // Atributo Valor como constante
    public final String NOME_RELATORIO;  // Atributo Nome Relatório como constante

    TipoPagamento(int valor, String nomeRelatorio) { // Construtor
        this.VALOR = valor;
        this.NOME_RELATORIO = nomeRelatorio;
    }

		// Método que irá nos retornar a enumeração basseado no atributo NOME_RELATORIO.
    public static TipoPagamento tipoPagamentoPorNomeRelatorio(String nomeRelatorio) {
				
//ForEach para percorrer as enumerações do values (DEBITO,CREDITO)
        for (TipoPagamento i : values()) {
            if (i.NOME_RELATORIO.equals(nomeRelatorio))// Se i tiver o atributo nome relatorio igual
                return i; //Retorna i
        }
        return null; // Caso não retorna null
    }
}
```