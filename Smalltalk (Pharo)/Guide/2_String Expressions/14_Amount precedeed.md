### Leer dos letras de teclado y luego un texto terminado en ‘/’. Se pide determinar la cantidad de veces que la primera letra precede a la segunda en el texto.

```smalltalk
| l1 l2 s1 c i let first_1|.

s1:= (UIManager default request: 'Enter a phrase finished with /: ').

l1:= (UIManager default request: 'Enter the first letter: ') first.

l2:= (UIManager default request: 'Enter the second letter: ') first.

Transcript clear.
Transcript show: 'Text: ', s1; cr.

s1:= s1 asLowercase.
l1:= l1 asLowercase.
l2:= l2 asLowercase.

c:= 0.
i:= 1.

first_1:= false.

[ (s1 at: i) ~= $/] whileTrue: [ 
	let:= (s1 at: i).
	(let = l1) ifTrue: [ 
		first_1:= true.
		 ] ifFalse: [ 
			(first_1) ifTrue: [ 
				 (let = l2) ifTrue: [ 
						c:= (c+1).
						first_1:= false.
					 ] ifFalse: [ 
						first_1:= false.	
					 ].
				 ].
		 ].
	
	i:= (i+1).
	
	 ].

Transcript show: 'Amount of times that the letters -', l1 asString, l2 asString, '- Appears consecutive are: ', c asString; cr.
```
