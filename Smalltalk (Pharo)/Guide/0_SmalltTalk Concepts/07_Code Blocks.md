### Code Blocks, remember that a bock can have arguments (Bloques de código, recordar que un bloque puede tener argumentos).

-A block in Pharo is a piece of code enclosed in square brackets [ ... ] that works like an anonymous function. It is a first-class object, which means that it can be stored in variables, passed as an argument to other methods, and executed later. To execute a block, the value message is used, which evaluates the code it contains and returns the result. Blocks can receive arguments, allowing you to encapsulate flexible logic that depends on external values.

-In addition, blocks are widely used for flow control, iterations, and filtering collections. Since they are objects, they can be combined with any object method and allow concise operations on characters, numbers, and other collections. For example, they can be used with methods such as isVowel to evaluate conditions on characters, or within collection methods such as select: to filter elements according to a criterion.

-In summary, blocks are a fundamental tool in Pharo that allow you to encapsulate logic that is executed on demand, make code more flexible, and take advantage of object-oriented programming even in small operations or conditions.


#### a)

```Smalltalk
[ $a isVowel ] value

Result: True

Note: isVowel allows you to determine whether a character is a vowel, returning true if it is. Therefore, evaluating [ $B isVowel ] value returns false. It does not matter whether the letter (character) is uppercase or lowercase; it detects it either way.
```

#### b)

```Smalltalk
[ $b isVowel ] value  

Result: false

Note: It is not a vowel
```

#### c)

```Smalltalk
[ 3+4. 'hola' asUppercase ] value

Result: 'HOLA'

Note: Is asUppercase, not asUpperCase, be careful with the capital in "case"
```

#### d)

```Smalltalk
| bloque |
bloque:=[ 'Hola ', ' como estás ?' ]. 
^bloque value.

Result: 'Hola  como estás ?'
```

#### e)
```Smalltalk
[ :c |  c isVowel ] value: $a

Result: True

NoteThis defines a code block that receives one argument, c. It returns true only if c is a vowel. In turn, value: $a executes the block, passing $a as the argument. The block evaluates $a isVowel → true.
If the character after value: is NOT a vowel, it returns false, as in this case:
```

#### f)
```Smalltalk
[ :c |  c isVowel ] value: $b 

Result: False

Note: b is not a vowel
```
#### h)
```Smalltalk
| bloque resp | 
bloque:=[ :a :b |  a , b]. 
resp:=bloque value: 'Hola ' value: ' como estás ?'. 
^resp

Result: 'Hola  como estás ?'

Explanation:
bloque := [ :a :b | a , b ]
-Defines a block with two parameters, a and b.
-Returns the concatenation of a and b.
resp := bloque value: 'Hola ' value: ' como estás ?'
-Executes the block, passing 'Hola ' as a and ' como estás ?' as b.
-The block concatenates the two strings.
^resp
-Returns the final result: 'Hola como estás ?'.
```
