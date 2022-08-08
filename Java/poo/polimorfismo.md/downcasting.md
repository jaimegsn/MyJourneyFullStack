#### Downcasting

É quando conseguimos através de uma variável de referência da superclasse acessar os atributos e métodos de uma subclasse.

- Não pode ser implícito pois nem sempre essa conversão será possível.
- Pode ocasionar a exceção de  ClassCastException
- Não é possivel fazer o downcasting de um objeto de superclasse para subclasse, mas sim em uma variável do tipo superclasse que está recebendo um objeto de subclasse.

Imaginando no contexto:  Produto(Superclasse)  -  Computador(Subclasse)

Inicialmente é igual ao upercasting, temos uma variavel de referencia de uma superclasse sendo atribuída a uma subclasse EX:

```java
Produto p1 = new Computador(400, "Positivo", "P30"); // Valor,Nome,Modelo
```

Depois para conseguirmos ter acesso aos método e atributos da subclasse através da variável de referência da subclasse é necessário fazer um casting:

```java
System.out.println(((Computador) p1).getModelo()); // Output: 'P30'
```

### Outra formas de realizar o Donwcasting, porém segue a mesma lógica:

2° Forma :

```java
Computador c1 = new Computador(300, "Toshiba", "xrl8");
Produto p2 = c1;
System.out.println( ((Computador) p2).getModelo() );
```

3° Forma em Métodos com instanceOf:

O instanceOf verifica se aquele objeto pertence realmente a classe que estamos querendo acessar para evitar erros:

```java
Computador c2 = new Computador(500, "Asus", "A300"); // Argumento do tipo Computador
downCastingMetodo(c2); // Sabendo que o parâmetro é do tipo Produto

public static void downCastingMetodo(Produto produto) {
	if (produto instanceof Computador) { // Verifica se Produto é uma instancia de Computador
		Computador computador = (Computador) produto; // Fazendo o casting
		// Outra forma de Casting:  ((Computador) produto).getModelo()
		System.out.println(computador.getModelo());
	}
}
```