#### Sobrescrita de Métodos

As classes filhas podem sobrescrever métodos da classe pai e adotarem um novo comportamento EX:

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

	@Override
	public void qtdPatas(){
		System.out.println("Tenho 2 patas");
	}
}
```

Note que na classe filha repetimos a o mesmo método da classe Pai, isso faz com que os objetos da classe Galinha ao chamar esse método atenda ao comportamento da classe Galinha e não da Classe Animal.   Logo o método foi sobrescrito.

E sobre o indicador @Override, é importante coloca-lo pois caso seja colocado parâmetros ou nome diferentes do método que estamos sobrescrevendo ele indicará que está errado na IDE 

[Método toString (Sobrescrita)](tostring.md)