### A partir de una frase ingresada por el usuario contar la cantidad de palabras que empiezan con una determinada letra (también ingresada por el usuario). 

```smalltalk
| s1 cp let start|.

Transcript clear.

s1:= (UIManager default request: 'Enter a phrase: ').
let:= (UIManager default request: 'Enter a letter: ') first.

Transcript show: 'The phrase is: ', s1; cr.
let:= let asLowercase.
s1:= s1 asLowercase.

cp:= 0.
start:= true.

s1 do: [ :i |
	(start) ifTrue: [ 
		(i = let) ifTrue: [ 
			cp:= cp + 1.
			start:= false.
			 ] ifFalse:[
			start:= false
			].
		 ] ifFalse: [ 
		(i = $ ) ifTrue: [ 
			start:= true.
			 ].
		 ].
	 ].


Transcript show: 'The amount of words started by the letter -', let asString, '- is: ', cp asString; cr.

Transcript cr.

```
