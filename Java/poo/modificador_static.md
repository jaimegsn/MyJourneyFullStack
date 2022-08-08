#### Modificador Static

A característica do modificador static é não depender de objetos então eles são chamados pelo nome da classe ex: CampoFutebol.area.

##### EM ATRIBUTOS:

Um atributo com o modificador static fica atrelado a classe, e se for alterado isso irá refletir em todos os objetos instanciados daquela classe. por exemplo se eu crio uma classe CampoFutebol com o atributo estático area=40  e instancio 3 objetos campo1, campo2 e campo3 se eu mudo o valor de area para  area=50  os 3 objetos irão sofrer essa mudança. 

```java
public class CampoFutebol {
    private static double area = 40;
		public static String teste = "Public consegue acessar direto da main";
		public void mudarArea(){
			CampoFutebol.area=50;
		}
}
public class Main{
	public static void main(String[] args){
			CampoFutebol.teste="Se for no mesmo pacote não precisa de import do pacote";
	}
}
```
<hr>
##### EM MÉTODOS:

Em métodos o modificador estático indica que o método não precisa da instância do objeto para ser chamado e não é permitido usar o this dentro do escopo de um método static, porquê métodos e atributos estáticos em java são carregados antes da instancia de qualquer objeto e com isso ele não têm acesso ao objeto.

```java
// Classe CampoFutebol
package introducao;
public class CampoFutebol {
    private static double area = 40;
    private String nome = "Castelão";
    
    public static void alterarArea(double area){ // Método estático
        CampoFutebol.area = area;
				this.nome = "Castelão Boladão"; // Não é permitido utilizar o THIS
    }
		public static double getArea() { // Método Estático
        return CampoFutebol.area;
    }
}

//Classe Main
package introducao;

public class DevDojo {
    public static void main(String[] args) {
        CampoFutebol .alterarArea(50); //Chamando método estático sem nenhum objeto
        System.out.println(CampoFutebol.getArea());
    }
}
```