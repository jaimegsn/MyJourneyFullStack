#### Try With Resources

Em Java, a instrução **Try-with-resources** é uma instrução try que declara um ou mais recursos nela. Um recurso é um objeto que deve ser fechado assim que seu programa terminar de usá-lo. Por exemplo, um recurso de arquivo ou um recurso de conexão de soquete. A instrução try-with-resources garante que cada recurso seja fechado no final da execução da instrução. Se não fecharmos os recursos, isso pode constituir um vazamento de recursos e também o programa pode esgotar os recursos disponíveis para ele.

Você pode passar qualquer objeto como um recurso que implementa *java.lang.AutoCloseable* , que inclui todos os objetos que implementam java.io.Closeable.

Com isso, agora não precisamos adicionar um bloco final finally. Os recursos serão fechados assim que o bloco try-catch for executado.

Exemplo 1 recurso:

```java
try(Reader reader = new BufferedReader(new FileReader("teste.txt"))){ // Iniciando recurso
	// Trecho código try
}catch (FileNotFoundException e){
	e.printStackTrace();
}catch (IOException e){
	e.printStackTrace();
}
```

Exemplo com multiplos recursos, eles são fechado na ordem de baixo para cima:

```java
try(Recurso recurso1 = new Recurso();
		Recurso recurso2 = new Recurso();) { // Iniciando multiplos recurso

}catch(IOException e ){
	e.printStackTrace();
}
```