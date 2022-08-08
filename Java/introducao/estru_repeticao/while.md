#### While

Verifica se a condição entre parêntese do WHILE é verdadeira para executar o LOOP

```java
int i = 0;
while(i<=9){
	i = i + 1;
	System.out.println( i );
}

// Outro exemplo criando while infinito e quebrando o laço com BREAK
int i = 0;
while(true){
	i +=1;
	System.out.println(i);
	if(i==3) break;
}
```