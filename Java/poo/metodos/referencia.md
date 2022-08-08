#### Parâmetros do tipo por Referência

Nos parâmetros que se referenciam a um objeto tem que existir um tratamento diferente, pois não são gerado cópias do objeto, o argumento do escopo principal e o parâmetro no escopo do método estão apontando para o mesmo objeto, o mesmo endereço de memória.

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