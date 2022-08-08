#### Interfaces

- Uma interface é um conjunto de métodos públicos, sem implementação, que deverão ser implementados pela classe que utiliza essa interface.
- Uma interface não pode ser instanciada, mas pode ter uma variável referenciando e atribuindo um objeto de uma classe que está implementando ela, mais detalhes em Programação Orientada a Interface:
    
    [Programação Orientada a Interface](../polimorfismo.md/poi.md)
    

- Uma classe pode implementar diversas interfaces
- Costuma-se dizer que uma interface é uma classe 100% abstrata.  Todos os métodos assinados são públicos e abstratos, mesmo que não seja adicionado explicitamente em sua assinatura
- É útil quando você quer que classes tenham métodos com a mesma assinatura mas implementações diferentes, você cria uma interface para definir assinatura destes métodos.
- As classes então implementam eles da maneira que querem.
- Os atributos em interfaces sempre serão  public static final mesmo que não seja definido na sua criação, ou seja  constantes públicas e que não representa o estado de um objeto.
<br>

- [Exemplo](exemplo.md)

- [Múltiplas interfaces](multiplas.md)

- [Default ( Métodos Concretos)](default.md)