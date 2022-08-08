#### Errors, Exceptions, RuntimeExceptions..

Em java temos a classe Throwable que atua como a raiz da hierarquia de erros e exceções, dentro dessa classe temos a divisão de Errors e Exceptions.

Errors:

"Erro" é uma condição crítica que não pode ser tratada pelo código do programa, é causado devido à falta de recursos do sistema e é irrecuperável, quando o erro é detectado, o programa terminará de forma anormal.

São classificados como unchecked pois o compilador não possui nenhum conhecimento sobre sua ocorrência e erros são definidos pelo pacote java.lang.Error.

Exemplos: Erro de estouro de pilha, Erro de falta de memória ou um Erro de travamento do sistema

e o código não é responsável por tais erros.

---

Exceptions:

Uma Exceção é causada por causa do código e é recuperável, Exceções são tratadas usando três palavras-chave "try", "catch" e "throw".

Em palavras simples, podemos dizer que os erros ocorridos devido ao código impróprio são chamados de exceções. Por exemplo, se uma classe solicitada não for encontrada ou um método solicitado não for encontrado. Esses tipos de exceções são devidos ao código no programa, o sistema não é responsável por esses tipos de exceções.

As exceções são classificadas como tipo checked ou unchecked a diferença é que:

Checked: É detectada durante o periodo de compilação, quando você está digitando o código e o java obriga você a tratar aquela exceção, são definidas pelo pacote java.lang.Exception

Unchecked: É detectada apenas durante o tempo de execução, e o desenvolvedor não é obrigado a tratar aquela exceção.   São definidas pelo pacote java.lang.RuntimeExceptions que é uma subclasse de java.lang.Exception

RuntimeExceptions e Exceptions, são classes mais gerais que abrange diversas exceções é sempre bom identificar exceções mais específicas que são subclasse das mesmas citadas EX:

`IOException` é uma classe de exceção base para exceções geradas ao acessar informações usando fluxos, arquivos e diretórios. e é uma subclasse Exception ou seja ela é checked também, e em métodos que mechem com diretórios é mais interessante usar ela do que o Exception apesar de ser possivel.

outro exemplo é o :

`IllegalArgumentException` é uma classe de exceção que identifica em métodos quando um argumento sempre é inválido, por exemplo, números negativos, referências nulas, etc. e é uma subclasse da classe RuntimeExceptions ou seja ela é unchecked também, e é mais interessante utilizar ela nesses casos do que o RuntimeExceptions apesar de ser possível.

---

[Métodos importantes](metodos.md)