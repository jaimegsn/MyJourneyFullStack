#### Classes

Classes representam o molde que dará inicio a diversos objeto que serão instanciados depois. 

aqui um exemplo:

```java
public class Cachorro {
	public int patas = 4;
	private String som = "auau";

	public void emitir_som(){
		System.out.println(this.som)
	}
}
```