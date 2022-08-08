#### Alguns métodos String

```java
String nome = "jaime";
nome.charAt(0); // Trata a String como array e retorna o caractere da posição, no caso (J)
nome.length();  // Retorna a quantidade de caractere que aquela String possui
nome.toLowerCase(); // Retorna toda a String como minuscula
nome.toUpperCase(); // Retorna toda a String como MAIUSCULA
nome.replace("i","s"); // Troca um caractere na String -> "oldChar","newChar" (jasme)

nome.substring(2,4); // Retorna a String a partir daquele index, 2arg indica onde terminar(opcional) -> (im)

nome.trim(); // Retorna a String eliminando espaços desnecessários
nome = nome.concat("teste"); // Mesmo que nome+="teste";
nome.contains("mundo");// Retorna True se em Nome contém a palavra Mundo
nome.indexOf("mundo");// Retorna em qual indice começa palavra Mundo
nome.lastIndexOf("mundo");// Retorna o indice da ultima ocorrencia da palavra mundo
```