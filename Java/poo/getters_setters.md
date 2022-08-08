#### Getters e Setters

Como uma medida de segurança e boa prática, definimos os atributos de uma classe como private e acessamos através de métodos getters e mudamos ele através de métodos setters:

```java
public class Cadeira {
    private String cor = "vermelho";
    private String material = "madeira";

    public String getCor() { // Acessando o atributo cor
        return cor;
    }
    public void setCor(String cor) { // Mudando o atributo cor
        this.cor = cor;
    }
    public String getMaterial() { // Acessando o atributo material
        return material;
    }
    public void setMaterial(String material) { // Mudando o atributo material
        this.material = material;
    }
}
```