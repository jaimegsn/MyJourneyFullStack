#### Classes Abstratas

Classes abstratas representam uma ideia com características e comportamento, por exemplo você nunca viu um mamífero, você ja viu um cachorro, um gato, vaca… mas nunca de fato um mamífero, porque mamífero é uma ideia que existe por meio do cachorro por exemplo.

Classes abstratas são feitas com o propósito de ser estendida ou herdada.

Regras:

- Classes abstratas não podem ser instanciadas, só herdadas
- Possui métodos e/ou métodos já implementados
- Quem herda a classe abstrata deverá implementar os métodos abstratos, e consequentemente herdará a implementação dos métodos já implementados
- É útil quando você precisa definir, o corpo dos métodos e se ainda assim precisar, pode criar métodos abstratos para serem implementados pela classe que herda ela.
- Caso várias classes usem a mesma implementação para diversos métodos, pode-se utilizar classes abstratas ao invés da interface. Assim implementando os métodos uma única vez
<br>

- [Exemplo Classe](exemplo.md)

- [Métodos abstratos](metodos.md)