#### Capturar Múltiplas Exceções

É possivel capturar multiplas exceções com repetidos blocos ‘catch’s do try catch porém é necessário se atentar a um detalhe:

O tratamento da exceção mais genérica deve ficar mais abaixo da especifica, pois ao ser lançada a exceção, ela vai percorrer os ‘catch’s em ordem de cima para baixo e o primeiro que a exceção se encaixar vai ser o catch executado e o resto é ignorado, então se a ordem estiver mal feita o lançamento de exceção pode acabar encontrando primeiro um tratamento para um exceção generalizada como por exemplo RuntimeException em vez de um mais especifico como IllegalArgumentException.

EX (correto):

```java
try {
   criarNovoArquivo();
} catch (IOException e) { // Especifico
   e.printStackTrace();
} catch (Exception e){ // Generico
   e.printStackTrace();
}
```

O número de ‘catch’s possiveis é ilimitado
<br>
##### Multi Catch em Linha:

também é possivel capturar váris exceções em uma linha apenas usando operadores lógicos a regra que deve ser obedecida é não colocar exceções de mesma hierarquia de herança no multi catch e também a variável ‘e’ do catch quando ele tem multiplas exceções dentro dele vira uma constante final,  ex de multi catch:

```java
try {
   criarNovoArquivo();
} catch (IOException | IllegalArgumentException e) { // Várias exceções em uma linha
   e.printStackTrace();
} catch (Exception e){ // Mais Generica
   e.printStackTrace();
}
```