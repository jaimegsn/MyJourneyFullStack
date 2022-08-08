#### Arrays

Arrays é uma coleção sequencial que permite armazenar dados do mesmo tipo, e esses dados são chamados de elementos

```java
public class App {
    public static void main(String[] args) {
        // Sintaxe: tipoDado[] nomeArray = new tipoDado[tamanhoArray]
        double[] salario = new double[5];
        salario[0]=1;  // Atribuindo um elemento ao array na posição 0

        // Criando array e atribuindo dados diretamente
        int [] numeros = {1,2,3,4};
        System.out.println(numeros[0]); // Exibindo o 1° elemento que está na posição 0

				//Percorrer Array com ForEach
				for (int i : numeros) {
            System.out.println(i);
        }

				//Ordenar Arrays
				int[] nmrs = { 5, 3, 6, 1 };
        Arrays.sort(nmrs);

				// Para imprimir um array é necessario o toString  ou podemos fazer um foreach
				System.out.println(Arrays.toString(nmrs));

				// Como comparar Arrays:
				int[] n1 = { 5, 3, 6, 1 };
        int[] n2 = { 5, 3, 6, 1 };
        System.out.println(Arrays.equals(n1, n2)); 
    }
}
```

Lembrando que não é possivel aumentar/diminuir o tamanho do array em tempo de execução, para isso temos o ArrayList