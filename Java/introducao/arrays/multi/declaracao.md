#### Declaração e Atribuição

```java
package introducao;
public class DevDojo {
    public static void main(String[] args) {
        int[][] numeros = new int[2][2];
        numeros[0][0]=1;
        numeros[0][1]=2;

        numeros[1][0]=4;
        numeros[1][1]=5;

			//Também podemos inicializar com o 2°,3°.. array vazio e inicializa-lo depois, menos o primeiro
			int[][] numeros2 = new int[2][];

			//Podemos inicializar já com os valores
			// Array[4] : [0]->[3];  [1]->[3];  [2]->[4];  [4]->[3];
        int[][] numeros = {{1,2,3},{3,2,1},{1,2,3,4},{1467,21,23}};
    }
}
```