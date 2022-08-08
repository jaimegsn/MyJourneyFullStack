#### Herança

Em Java quando duas ou mais classes possuem atributos e métodos que se repetem, é possível remover esses atributos e métodos dessas classes criar uma nova classe que irá conter todos esses métodos e atributos que se repetem e defini-lo como uma superclasse ou classe pai, e fazer com que as classes que antes tinham métodos e atributos repetidos diversas vezes apenas herdem os atributos e métodos da classe pai sem precisar rescrever o código.

Em outras palavras herança é quando uma classe pode herdar os atributos/métodos de outra classe, a classe que tem os seus atributos e métodos herdados é chamado de superclasse ou classe pai, enquanto que a classe que herda é chamado de subclasse ou classe filho. 

Porém vale lembrar que a classe pai não tem acesso aos atributos da classe filho.

Por exemplo: Superclasse animal e sub-classes como cachorro, gato, papagaio..

Lembrando que atributos private não são herdados

- [Exemplo](exemplo.md)

- [Sobrescrita de Métodos](sobrescrita.md)

- [Super](super.md)

- [Construtores](construtor.md)

- [Modificador Final em Método](../modificador_final/final_metodo.md)

- [Modificador Final em Classes](../modificador_final/final_classe.md)

Dar atenção ao modificador de acesso protected:
[Modificador de acesso (Visibilidade)](../modificador_acesso.md)