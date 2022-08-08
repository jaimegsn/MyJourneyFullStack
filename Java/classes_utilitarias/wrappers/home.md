#### Wrappers

Os tipos primitivos possuem certas limitações por não possuir métodos que adicionem funcionalidades a eles, pensando nisso o java criou os Wrappers que são classes que possuem o mesmo tipo de dados dos tipos primitivos, outro motivo para a criação dos Wrappers é para existir a possibilidade de se passar parâmetros do tipo referência nos métodos com os dados primitivos, além de que listas só aceitam Wrappers.

```java
Byte byteW = 127; // byte
Short shortW = 4; // short
Integer intW = 3; // int
Long longW = 4L; // long
Float floatW = 3F; // float
Double doubleW = 4D; // double
Character charW = 'Á'; // char
Boolean booleanW = true; // boolean
```

Sempre tente usar tipos primitivos, só use Wrappers nas situações devidas para ele, como listas, threads, passagem de parâmetro como tipo de referência…

Os Wrappers tem métodos interessantes e nativos para cada tipo, como é trabalhoso listar todos, pesquise bastante se algo que você deseja já não existe na manipulação desses tipos de dados antes de implementar algo na mão.

Por exemplo o Character possui métodos de verificar se uma caractere é um digito com o Character.isDigit(char), verificar se é uma letra com o Character.isLetter(char)…

- [Autoboxing](autoboxing.md)

- [Unboxing](unboxing.md)

- [Converter String em Wrapper](converter_string.md)