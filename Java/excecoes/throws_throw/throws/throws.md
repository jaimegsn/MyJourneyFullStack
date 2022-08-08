#### Throws

Caso um método precise lançar uma exceção, mas você não deseja tratar dentro do escopo do método, você pode avisar que aquele método precisa ser tratado quando ele for chamado, basta utilizar a palavra chave `throws`no final da assinatura do método.

Quando utilizamos o `throws`precisamos também informar qual ou quais exceções podem ser lançadas.

EX:

```java
public void criarNovoArquivo() throws IOException{
        File file = new File("arquivo\\teste.txt");
        file.createNewFile();
        System.out.println("Arquivo criado");
    }

// Pode ser colocado mais de uma exceção:
public static int divisao(int a, int b) throws IllegalArgumentException,IOException{
	if(a==0 || b==0) throw new RuntimeException("Argumento inválido");
	return a/b;
}
```

Existe também uma forma hibrida de você tratar a exceção e permitir que quem for chamar a exceção também possa trata-la usando o Try Catch, basta ir no catch e relançar a exceção com throw como unchecked e passando o objeto criado no Catch como parâmetro.

EX:

```java
public static void divisao() throws RuntimeException{
      File file = new File("diretorio/pasta");
      try{
	      file.createNewFile();
      }catch(IOException e){
       // Trata aqui e relança com throw
	      throw new RuntimeException(e);
      }
}
```

[Regras em Sobrescrita de métodos](sobrescrita.md)