#### Finally

A palavra-chave `finally`representa um trecho de código que será sempre executado, independentemente se uma exceção ocorrer.

EX:

```java
	  try {
      /* Trecho de código no qual uma
       * exceção pode acontecer.
       */
    } catch (Exception e) { // Note que o 'e' é um objeto instanciado da classe Exception
      /* Trecho de código no qual uma
       * exceção do tipo "Exception" será tratada.
       */
    } finally{
			/* Trecho de código que sempre será executado
       * independente se ocorreu alguma exceção ou não.
       */
		}
```

EXTRA → exemplo de boa prática:

Durante o desenvolvimento de algum projeto é comum diversas vezes realizar a solicitação de algum recurso, pode ser do sistema operacional (S0) por exemplo solicitar a abertura de um arquivo, escrita, solicitar também recursos de um banco de dados e etc.

Então é preciso gerenciar esses recursos fechando ele após a sua utilização pois caso não o faça pode deixar o sistema mais lento caso aquele recurso esteja sendo acessado por múltiplos clientes.

Também é comum durante o acesso a esses recursos ocasionar diversas exceções então para trata-las é comum utilizar o try e o catch, porém se fecharmos o recurso durante o try é perigoso pois, ao ocorrer uma exceção todo o código do try abaixo da linha que ocorreu a exceção é ignorado, então imagine que você acessou o recurso e durante a manipulação desse recurso foi lançada uma exceção a linha de código que fechava esse recurso não foi executada, então é aconselhado que esse recurso seja fechado no FINALLY.