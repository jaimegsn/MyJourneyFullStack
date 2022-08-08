#### Throws, Throw , Try Catch e Finally

- [Try Catch](try_catch/trycatch.md)

- [Finally](finally.md)

- [Throw](throw.md)

- [Throws](throws/throws.md)

Então resumidamente : 

- O Try Catch percebe uma exceção lançada e trata ela.
- O Throw lança uma exceção manualmente pelo código
- O Throws avisa que um método pode lançar um exceção, para quem o estiver chamando trata-lo com try catch

Importante também notar que em situações em que o método é privado faz mais sentido usar o Try Catch, pois não será possível chamar o método para trata-lo .