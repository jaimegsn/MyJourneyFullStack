#### Operadores Relacionais/Comparação

Usado para comparar dois valores

- '=='  → igualdade e retorna True se dois valores são iguais.
- '!='  → diferença e retorna True se dois valores são diferentes.
- '>'  → maior que e retorna True se um valor é maior que o outro.
- '>='  → maior ou igual e retorna True se um valor é maior ou igual ao outro.
- '<'   → menor e retorna True se um valor é menor que o outro.
- '<='  → menor ou igual e retorna True se um valor é menor ou igual ao outro.

```java
var x = 5;
x+=2;
if(x > 1){
	System.out.println("Olá Mundo");
}
...
..
```

Comparar String

```java
var x = "jaime";
if(x.equals("jaime"){
	System.out.println("É igual");
}
```

Verificar se um objeto percence a determinada classe

```java
Gato gato1 = new Gato();
if(gato1 instanceof Gato) System.out.println("Gato 1 pertence a classe GATO");
```