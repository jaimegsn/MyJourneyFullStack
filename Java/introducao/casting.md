#### Casting de Tipos Primitivos (Conversão)

> O único tipo que não se encaixa aqui é o BOOLEAN.
> 

Casting é o termo que se dá quando você atribui a uma variável/atributo de um certo tipo, a um dado de outro tipo, EX: Float → Double, Long → Int….

E temos as nomenclaturas :

- Widening Casting (automático) - converte um tipo menor para um tipo maior
    
    byte -> short -> char -> int -> long -> float -> double
    
    ```java
    double variavelDouble = 5.3F;
    int variavelINT = 30;
    int variavelLONG = variavelINT; 
    ```
    

- Narrowing Casting (manual) - converte um tipo maior para um menor requer -> (type) e se o valor for muito alto para a conversão o dado fica impreciso e pode apresentar problemas.
double -> float -> long -> int -> char -> short -> byte
    
    ```java
    float variavelFloat = (float) 2.5;
    char variavelCHAR = 'a';
    byte variavelBYTE = (byte) variavelCHAR;
    
    ```