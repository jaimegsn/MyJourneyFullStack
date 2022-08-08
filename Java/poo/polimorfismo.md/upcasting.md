#### Upcasting

É quando criamos uma variável do tipo da classe pai recendo um objeto da classe filha.

Em outras palavras converter um objeto da classe filha para um objeto da classe pai.

- Sempre funciona pois o objeto filho é sempre compatível com o objeto pai
- Pode ser feito implicitamente
- Apenas os métodos e atributos da classe pai funcionam

Basicamente tudo que referência a classe pai pode receber o objeto filho, como parâmetros, variáveis….

Classe Main:

```java
public class Main {
    public static void main(String[] args) {
        //Upcasting
        Animal animal1 = new Cachorro("Chico", "Animalias", 4);
        System.out.println(animal1.getNomeCientifico());
        System.out.println(animal1.getPatas());

    }
}
```

Classe Pai:

```java
public class Animal {
    private int patas;
    private String nomeCientifico;

    public Animal(int patas, String nomeCientifico) {
        this.patas = patas;
        this.nomeCientifico = nomeCientifico;
    }

    public int getPatas() {
        return patas;
    }

    public String getNomeCientifico() {
        return nomeCientifico;
    }

}
```

Classe Filha:

```java
public class Cachorro extends Animal {
    private String nome;

    public Cachorro(String nome,String nomeCientifico, int patas) { // Construtor
        super(patas,nomeCientifico);
        this.nome = nome;
    }

    public void latir() {
        System.out.println("auaua");
    }

    public String getNome() {
        return nome;
    }

}
```