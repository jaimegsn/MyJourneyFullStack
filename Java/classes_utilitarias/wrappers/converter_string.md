#### Converter String em Wrapper

O único que não possui esse método é o Character, até porque não faz muito sentido, quanto ao resto é possivel com o método parse:

```java
Byte byteNum = Byte.parseByte("125");
Short shortNum = Short.parseShort("12");
Integer integerNum = Integer.parseInt("32");
Long longNum = Long.parseLong("81");
Float floatNum = Float.parseFloat("23.1");
Double doubleNum = Double.parseDouble("40.5");
Boolean booleanState = Boolean.parseBoolean("true");
```