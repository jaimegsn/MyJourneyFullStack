#### Strings, String Builder, String Buffer

As String representam um tipo de dado de texto, mas como funcionam ?

Todas as Strings são imutáveis, o que acontece por de trás é que é gerado um String Constant  Pool, uma piscina de strings onde ao criar uma String como no exemplo:

```java
String nome = "jaime";
```

A String “jaime” é adicionada na pool(piscina), e ao criar uma segunda string recebendo o valor também de “jaime” como no exemplo:

```java
String nome2 = "jaime";
System.out.println(nome==nome2); // True
```

Não é gerado uma String nova, a variavel ´nome2´ e a ´nome´ estão apontando para o mesmo endereço de memória da String “jaime”.

E os valores que estão na pool strings são constantes e imutáveis, ou seja quando se concatena uma string, transforma ela de alguma maneira, é gerado uma nova string na pool e não é alterado a antiga.

Uma maneira de gerar uma nova String com o mesmo valor e fora da pool é criando um novo objeto do tipo String visto que String é uma classe, porém é feio fazer isso no código e desnecessário

- [Alguns Métodos String](metodos.md)

- [Desempenho](desempenho.md)

- [String Builder](string_builder.md)