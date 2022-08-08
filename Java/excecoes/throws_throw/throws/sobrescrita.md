#### Regras em Sobrescrita de métodos

Caso o método original tenha uma exceção no throws, o método que sobrescrever ele pode ou não adicionar o throws, se o fizer ele tem que se adequar ao método principal baseado na hierarquia das classes de exceções, colocando a mesma exceção ou uma abaixo da hierarquia, nunca acima.

Ainda é possível adicionar mais exceções além do da original ou sem o da original, obedecendo a hierarquia.