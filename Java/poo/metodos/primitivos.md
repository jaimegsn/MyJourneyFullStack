#### Parâmetros do tipo Primitivo e Wrappers

É recomendado que se gere cópias dos argumentos passados nos parâmetros, para que a variável original não perca seu valor. Com os tipos primitivos e wrappers isso não é uma preocupação, no Java mesmo já ocorre esse processo o valor da variável/argumento do escopo principal não será afetado pelo que acontecerá com o parâmetro no escopo do método, isso ocorre porquê ambos estão apontando para diferentes endereços de memória. 

EX:

```java
// Escopo principal
public static void main(String[] args){
	int x = 5;
	metodoTeste(x); // Método teste passando X como parâmetro primitivo
}

//Escopo método
public static int metodoTeste(int numero){
	return numero * 50;
}
```