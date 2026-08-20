#### Comparing Objetct. Evaluate each one, check the results and in case of an error, indicate the correct expression (Comparando Objetos. Evaluar c/u, verificar resultados y en caso de error indicar la expresión correcta).

#### a)
```smalltalk
3 < 4

Result: True
```

#### b)
```smalltalk
#( 1 2 3 4) = #(1 2 3 4) 

Result: True
```

#### c)
```smalltalk
'hola' <= 'adios'  

Result: False

Clarification: In Pharo, strings are compared lexicographically, that is, character by character according to the ASCII value of each letter. Therefore, as soon as a pair of different characters is found, the comparison is determined by those characters, and the following ones are not compared.
So, for this example:
-The first character of each string is compared: 'h' (ASCII 104) and 'a' (ASCII 97).
-Since 104 > 97, 'hola' is not less than or equal to 'adios'.
-Therefore, the comparison returns false.
```

#### d)
```smalltalk
5 = 2 + 3

Result: ERROR

Clarification: As written, this will return an error because it is read as 5 = 3, a message sent to 5 with 3 as its argument, and then it tries to apply + 2 to the result (true or false) → error, because you cannot do true + 2.
```

#### e)
```smalltalk
5 = (2 + 3)

Result: True
```
