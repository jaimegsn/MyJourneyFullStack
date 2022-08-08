#### Inicializar

Quando declaramos o array multidimensional com o 2° array em diante vazio podemos inicializa-lo depois no código:

```java
package introducao;

public class DevDojo {
    public static void main(String[] args) {
        int[][] numeros = new int[4][];

        // Inicializando
        numeros[0] = new int[2]; // Apontado o numeros[0] para um novo array de 2 posições
        numeros[1] = new int[4]; // Apontado o numeros[1] para um novo array de 4 posições
        numeros[2] = new int[] { 7, 8, 9 }; // Apontado o numeros[22] para um novo array e ja atribuindo valores

        // Atribuindo valores:
        numeros[0][0] = 1;
        numeros[0][1] = 2;

        numeros[1][0] = 3;
        numeros[1][1] = 4;
        numeros[1][2] = 5;
        numeros[1][3] = 6;

        // Apontando para um array já criado
        int[] nl = new int[]{10,0};
        numeros[3] = nl;
    }
}
```