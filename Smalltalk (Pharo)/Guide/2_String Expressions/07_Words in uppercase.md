### Dada una frase contar la cantidad de palabras en mayúsculas. 

```smalltalk
| s1 cm |

Transcript clear.

s1:= (UIManager default request: 'Enter a phrase: ').

cm:= 0.

s1 do: [ : i|
	(i isUppercase) ifTrue: [ 
		cm:= cm + 1
		 ].
	
	 ].

Transcript show: 'The phrase -', s1, '- has ', cm asString, ' uppercases.'
```
