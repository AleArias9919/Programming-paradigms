####  Nested_Messages. Evaluate them and, if it is neccesary, add parentheses to show how Smalltalk evaluates the expressions (Mensajes anidados. Evaluarlos y de ser necesario, colocar paréntesis para mostrar de qué manera ST evalúa las expresiones.)


#### a)
```smalltalk
'hola' size + 4

Result: 8
```

#### b)
```smalltalk
'ahora' size + #( 1 2 3 4 ) size

Result: 9
```

#### c)
```smalltalk
#( 1 12 24 36) includes: 4 factorial

Result: True
```

#### d)
```smalltalk
3 + 4 * 2 

Result: 14
```

#### e)
```smalltalk
3 + ( 4 * 2 )

Result: 11
```

#### f)
```smalltalk
4 factorial between: 3 + 4 and: 'hola' size * 7 

Result: true

Note: It checks if the factorial of 4 (24) is between 3 + 4 = 7 and 'hello' size * 7 = 28. Since 24 is within the range, return true.
```

#### g)
```smalltalk
'hola' at: ( #( 5 3 1 ) at: 2 ) 

Result: $l

Note: First, the at: of the array ( #(5 3 1) at: 2 ) = 3 is evaluated. Then, 'hola' at: 3 returns 'l'.
```

#### h)
```smalltalk
(6 + 9) asString 

Result: '15'
```

#### i)
```smalltalk
Array with: 1 with: 'hola' with: (1/3)

Result: {1. 'hola'. (1/3)}
```

