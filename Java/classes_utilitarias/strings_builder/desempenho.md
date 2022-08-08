#### Desempenho

A utilização de muitas Strings acaba prejudicando o desempenho do sistema, como por exemplo em um looping que concatena várias String acaba precisando de muito espaço de memória no String Constant Pool e vai deixando o sistema cada vez mais lento.

Então em casos que percebe-se que o sistema está ficando lesado por conta do uso de String, existem outras duas classes que são mais otimizadas, porém só se deve utiliza-las nesses casos para fins de otimização:

São as clases String Builder ou String Buffer, as duas são parecidas na prática mas muda na forma em que tratam a String, o buffer é thread safe enquanto o builder não. 

Consequentemente o Builder é mais rápido porém não possui a segurança multi-thread que o Buffer possui, porém nem sempre essa segurança se faz necessária por isso existe essas duas classes separadas.