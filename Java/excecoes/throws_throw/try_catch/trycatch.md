#### Try Catch

Para tratar possíveis exceções temos o try e o catch, onde o try vai tentar executar um trecho de código e pode ocorrer tudo bem, mas caso aconteça uma exceção o catch vai capturar essa exceção e executar um bloco de códigos com a finalidade de tratar esse problema.

Então para exemplo vamos testar com o método chamado createNewFile da classe File, onde o seu propósito é criar um arquivo, esse método ele é checked então é obrigatório o seu tratamento no código.

Sintaxe:

```java
try {
      /* Trecho de código no qual uma
       * exceção pode acontecer.
       */
    } catch (Exception e) { // Note que o 'e' é um objeto instanciado da classe Exception
      /* Trecho de código no qual uma
       * exceção do tipo "Exception" será tratada.
       */
    }
```

Ex:

```java
public static void main(String[] args) {
        File file = new File("arquivo\\texto.txt"); // Instanciamento da classe FILE
        try{ 
            file.createNewFile();
        }catch(IOException e){ 
	        e.printStackTrace(); // Chama o método printStackTrace da classe Exception já que IOExceptions é uma subclasse de Exception
        }
    }
```

o objeto ‘e’ instanciado da classe IOException pode ser re-lançado com o throw new, ao fazer isso devemos usar o throws no método

- [Capturar Múltiplas Exceções](multiplas.md)

- [Try With Resources](trywithr.md)