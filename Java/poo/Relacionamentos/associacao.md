#### Associação

Associação é o relacionamento que está mais ligado ao verbo ter, por exemplo quantos cursos um aluno pode ter ?, quantos alunos um curso pode ter ?, uma escola tem quantos professores ?.

Na prática em Java quando temos a associação entre duas classes por exemplo Escola e Professor,

adicionamos um campo em escola do tipo Professor, como são vários professores em uma escola o campo deve ser um array:

```java
Professor[] professores;
```

Já na classe Professor é apenas uma escola então adicionamos o campo escola na classe professor assim:

```java
Escola escola;
```

Então existe os seguintes tipos de relacionamentos

1→1 Um para Um (Sem Arrays de Objetos)

1→N ou N→1, depende da ordem de leitura, Um para Muitos ( Com um array de objeto em uma classe)

N→N Muitos para Muitos (Arrays de Objetos nas duas classes)