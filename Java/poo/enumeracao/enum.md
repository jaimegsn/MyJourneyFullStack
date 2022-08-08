#### Enumeração

Em Java quando queremos adicionar um campo na classe que tenha valores limitados e objetivos é interessante que se use o enum pois ele não permite que alguém erre ao inserir um dado nele.

Por exemplo o sexo de uma pessoa pode ser ‘M’ ou ‘F’, porém pode acontecer bugs se alguém inserir

‘m’ ou ‘f’ ou até mesmo ‘masculino’ se formos deixar isso como uma String, então para isso podemos criar um tipo enum e inserir as opções que podem ser digitadas.

As enumerações reduzem o número infinito de possibilidades de valores que podem ser atribuídos. Por exemplo, você pode limitar os meses do ano que um método recebe, no caso ele só receberia por exemplo dos meses de Janeiro a Junho e de Agosto até Novembro, se informado qualquer mês diferente disso poderia gerar um erro para o usuários.

No exemplo vamos fazer uma classe do tipo ENUM que irá atribuir o tipo do cliente, se ele é PESSOA_JURIDICA ou PESSOA_FISICA :

- [Exemplo Arquivo Separado](exemplo_separado.md)

- [Exemplo Dentro da Classe](exemplo_dentro.md)

Classes de Enumeração também possui mais recursos como por exemplo construtores:

- [Construtores, exemplo em Arquivos Separados](construtor_separado.md)

- [Construtores, exemplo dentro da classe](construtor_dentro.md)

Classes de Enumeração possuem métodos e eles podem ser sobrescritos

- [Sobrescrita de Métodos em Enumeração](sobr_met.md)

Busca por Atributos (Retornar uma enumeração baseada nos seus atributos) :

- [Exemplo busca por atributos](busca_atributo.md)