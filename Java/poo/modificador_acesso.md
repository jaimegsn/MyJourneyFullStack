#### Modificador de acesso (Visibilidade)

A visibilidade ela pode ser aplicada tanto em métodos quanto também em variáveis/atributos;  Ela é responsável por definir o escopo de acesso a aquela variável ou método.

Temos esses tipos de visibilidade:

- Public: A sua caracteristica é que qualquer arquivo dentro do mesmo pacote(pasta) pode acessar a variavel/método, as outras classes fora do pacote precisam importar o pacote onde está  a classe do método/atributo que deseja utilizar EX:
    
    ```java
    //Pacote: teste - Arquivo: App.java
    package teste;
    public class App {
        public static int x = 5;
        public static void main(String[] args) {
        }
    }
    
    //Pacote: teste - Arquivo: teste.java
    package teste;
    public class teste {
        public static void main(String[] args) {
            System.out.println(App.x); // <- Conseguimos acessar
        }
    }
    
    //Pacote: USER - Arquivo: teste2.java
    package user;
    import teste.App;   // NOTE O IMPORT 
    public class teste {
        public static void main(String[] args) {
            System.out.println(App.x); // <- Conseguimos acessar
        }
    }
    ```
    
- Private: Apenas a classe onde o recurso foi declarado tem acesso a ele EX:
    
    ```java
    package teste;
    public class App {
        private int x = 5;
    }
    ```
    

- Protected: o protected dá acesso a todas as classes que estiverem no mesmo pacote e a todas as suas sub-classes ou classes filhas
    
    ```java
    package teste;
    public class App{
    	protected int x =5;
    }
    ```
    

- Default:  É a visibilidade padrão e não precisa ser declarada, a sua característica é que qualquer classe dentro do mesmo pacote(pasta) pode acessar a variável/método, além da própria classe EX:
    
    ```java
    //Pacote: SRC - Arquivo: App.java
    public class App {
        static int x = 5;
        public static void main(String[] args) {
        }
    }
    
    //Pacote: SRC - Arquivo: teste.java
    public class teste {
        public static void main(String[] args) {
            System.out.println(App.x); // <- Conseguimos acessar
        }
    }
    ```