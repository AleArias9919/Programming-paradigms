#### Condictionals, check these expressions (condicionales, verifica estas expresiones) }

#### a)
```smalltalk
3 < 4 ifTrue: ['el bloque verdadero'] 
	ifFalse: ['el bloque falso'] 

Result: 'el bloque verdadero'
```


#### b)
```smalltalk
(5>2) ifTrue:[^’5 es MAYOR que 2’] 
	ifFalse:[^’5 es menor que 2’]. 

Result: Error — Unknown character

Note: In the first example, ^ is not used because the code is being evaluated in the Playground. In this environment,
-Pharo automatically displays the result of the last expression without requiring an explicit return.
-In the second case, ^ is included inside the block. When the condition is met, Pharo immediately returns that value and stops the execution of the method.
-In other words, nothing after the return is executed. It can also be used outside the Playground (in a method or class).
```

#### c)
```smalltalk
$b isVowel ifTrue:[^'es una vocal'] 
ifFalse:[^'es una consonante'] 

Result: 'es una consonante

Note: In this case, since the letter is b, which is not a vowel, the condition returns false, unlike the previous two examples. Therefore, the ifFalse: block is executed, and the result is: 'es una consonante'.
```
