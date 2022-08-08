#### String Builder

O String builder manipula dados também do tipo String, a diferença é que ao ser concatenada a String Builder não ocupa mais espaço no pool de Strings.

O String Builder é uma classe então podemos passar a String que queremos logo no construtor:

```java
StringBuilder sb = new StringBuilder("Aqui");
```

Ou então inserir posteriormente com append ou insert:

```java
StringBuilder sb = new StringBuilder();
sb.append(" alo ");
sb.append(" galera ");
sb.append(" de ");
sb.append(" cowboy ");

// Com insert passamos a posição e a string que queremos inserir
sb.insert(0,"a");
System.out.println(sb);
```