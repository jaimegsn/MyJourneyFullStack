#### Percorrer o ArrayMultidimensional

```java
package introducao;
public class DevDojo {
    public static void main(String[] args) {
        int[][] numeros = new int[2][2];
        numeros[0][0]=1;
        numeros[0][1]=2;

        numeros[1][0]=4;
        numeros[1][1]=5;
        

        //ForEach, iremos primeiramente percorrer o array base
        for (int[] retornoBase : numeros) { // Array base aponta/retorna outros arrays então tem que ser do tipo int[]
    
            for (int inteiros : retornoBase) { //Percorrendo o array retornado acima, irá nos retornar inteiros
                System.out.println(inteiros);
            }
        }
        //Fim ForEach

        // Outra forma de percorrer o Array Multidimensional com FOR:
        for (int i = 0; i < numeros.length; i++) {
            for (int j = 0; j < numeros[i].length; j++) {
                System.out.println(numeros[i][j]);
            }
        }
        //Fim
    }
}
```