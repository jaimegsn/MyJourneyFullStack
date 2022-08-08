#### Throw

Também é possível lançar uma exceção manualmente em alguma situação específica, como digitação incorreta de campos por parte do usuário ou algum problema identificado com uma estrutura de decisão por exemplo.

Quando lançamos uma Exceção, é interessante usa-lo juntamente com o trhows, para avisar que aquele método pode lançar uma exceção, principalmente se for uma exceção checked onde é obrigatório o uso do throws no método.

Sintaxe:

**`throw** **new** **<<** **Exceção** desejada **>>();**`

Exemplo :

```java
public static void main(String[] args) {
        System.out.println(divisao(2,0)); //Irá apresentar um bug de divisão por 0
    }

    public static int divisao(int a, int b) throws RuntimeException{
			// Se for detectado que algum dos argumentos é igual a 0
			// Lança uma exceção
		if(a==0 || b==0) throw new RuntimeException("Argumento inválido");
        return a/b;
    }
```

Também é possivel lançar um exceção do objeto criado no Catch do Try Catch, Ex:

```java
	try{
		criarNovoArquivo();
	} catch (IOException e) {
    e.printStackTrace();
		throw e("Caminho não encontrado"); <-AQUI
  }
```