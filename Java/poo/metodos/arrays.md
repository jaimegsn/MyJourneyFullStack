#### Parâmetro de Arrays

O array argumento que está no escopo principal e o Array parâmetro que está no escopo do método, ambos estão apontando para o mesmo endereço de memória, qualquer alteração em um, irá alterar o outro, portanto é necessário um tratamento diferente.

### Ex:

```java
package introducao;
public class DevDojo {

    public static void metodoNormal(int[] arr){ // Parametro para array
        System.out.println("Metodo normal -----");
        for (int i : arr) {
            System.out.println(i);
        }
    }

    public static void metodoMulti(int[][] arr2){ // Parametro para array Multidimensional
        System.out.println("Metodo Multi -----");
        for (int[] i : arr2) {
            for (int j : i) {
                System.out.println(j);
            }
        }
    }

    public static void metodoVarArgs (int... arr3){ // VarArgs para Array
        System.out.println("Metodo varArgs -----");
        for (int i : arr3) {
            System.out.println(i);
        }
    }

		public static void VarArgsParametro (int x,int... arr3){
    }

    public static void metodoVarArgsMulti (int[]... arr4){ //VarArgs para Array multidimensional
        System.out.println("Metodo varArgsMulti -----");
        for (int i[] : arr4) {
            for (int j : i) {
                System.out.println(j);
            }
        }
    }

    public static void main(String[] args) {
        int[][] multi = {{1,2,3},{1,2,3}};
        int[] normal = {1,2,3};

        metodoNormal(normal);
        metodoMulti(multi);

        metodoVarArgs(normal); 
				VarArgsParametro(5,normal); //Para mais de um parametro o VarArgs deve ser o ultimo
				metodoVarArgs(1,2,3,4); // O VarArgs aceita esse parâmetro

        metodoVarArgsMulti(multi);
    }
}
```