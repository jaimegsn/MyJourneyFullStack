#### Operadores Lógicos


Usado para verificar 2 comparações/afirmações

- && (AND)  retorna True se 2 afirmações ou mais forem verdadeiras

```java

System.out.println((5==5 && 5==5) ? "True" : "False"); // Retorna "True"
System.out.println((5==5 && 5==3) ? "True" : "False"); // Retorna "False"
```

- ||  (OR)  retorna True se uma das afirmações forem verdadeiras

```java
System.out.println((5==5 || 5==5) ? "True" : "False"); // Retorna "True"
System.out.println((5==5 || 5==3) ? "True" : "False"); // Retorna "True"
System.out.println((5==3 || 5==3) ? "True" : "False"); // Retorna "False"
```

- ! (NOT)  Reverte o retorno da operação se era para ser True vira False e vice-versa

```java
System.out.println(!(5==5 && 5==5) ? "True" : "False"); // Retorna "False"
System.out.println(!(5==3 || 5==5) ? "True" : "False"); // Retorna "False"
System.out.println(!(5==3 || 5==3) ? "True" : "False"); // Retorna "True"
```