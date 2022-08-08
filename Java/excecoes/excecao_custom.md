#### Exceções Customizada

Criar exceções customizadas em Java, é perfeitamente possível, e esta prática é usada largamente por diversos frameworks, como Hibernate, Spring, Struts entre outros vários.

- Uma exceção deve sempre terminar com o final Exception (semântico), ex: nomeException
- Para criar uma exceção basta herdar a classe RuntimeException ou Exception, ainda também é possível herdar as subclasses dessas classes.

EX:

```java
public class TesteException extends Exception{
    public TesteException() { // Caso não seja passado nenhuma mensagem no lançamento da exceção
        System.out.println("Login Inválido");
    }

    public TesteException(String message) { // Caso seja passado alguma mensagem no lançamento da exceção
        super(message);
    }
}
```