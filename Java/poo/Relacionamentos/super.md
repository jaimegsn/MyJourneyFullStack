#### Super

Assim como o this se refere ao objeto instanciado, o super se refere a classe Pai 

Então se temos um método sobrescrito na classe filho e queremos executar o método da classe pai

podemos fazer isso com super.

O super também consegue acessar atributos da classe pai se não for private.

Classe pai:

```java
public class Animal{
	public void qtdPatas(){
		System.out.println("Tenho 4 Patas");
	}
}
```

Classe filha:

```java
public class Galinha extends Animal{
	public void qtdPatas(){
		super.qtdPatas();  // Graças a referência super é executado o método da classe Animal  (Pai), porém ainda é pego os atributos do objeto caso eles sejam necessários dentro do método, porque o bloco de código do método da classe pai vai ter como referência o this
		System.out.println("Tenho 2 patas");
	}
}
```