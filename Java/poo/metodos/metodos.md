#### Métodos

Métodos se comportam como funções e representam comportamento/ações da classe(molde) daquele objeto, por exemplo a classe cadeira possui comportamentos de inclinar, diminuir altura…

Métodos podem ser vazios (void) ou podem retornar algum dado de algum tipo como String,int...

```java
public class Cadeira {

    // Métodos/Comportamentos Vazio:
    public void inclinar(){
        System.out.println("A cadeira está inclinada");
				return; //Funciona como um break para métodos vazios
    }

		// Métodos/Comportamentos que retornam algum tipo de dado:
    public int soma(){ // Retornando um inteiro
        return 5+5;
    }

		// Métodos com parâmetros:
		public int subtracao(int numero1, int numero2){
				return numero1-numero2;
		}
}
```

- [Modificador de acesso (Visibilidade)](modificador_acesso.md)

- [Modificador Static](modificador_static.md)

- [Parâmetros (Primitivos,Referencia,Arrays…)](parametros.md)