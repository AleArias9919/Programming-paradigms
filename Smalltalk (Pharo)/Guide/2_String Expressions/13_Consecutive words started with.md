###  Dado un texto terminado en ‘/’ determinar cuántas veces tres palabras seguidas comienzan con la misma letra. 

```smalltalk
| s1 cp let i plet clet start |.

i:= 1.
cp:= 0.

Transcript clear.

s1:= (UIManager default request: 'Enter the text: ' ).
Transcript show: 'Text: ', s1; cr.
s1:= s1 asLowercase.

start:= true.
clet:= 0.
plet:= (s1 at: 1).

[ (s1 at: i) ~= $/ ] whileTrue: [ 
	let:= (s1 at: i).
	(start) ifTrue: [ 
		(plet = let) ifTrue: [ 
			clet:= (clet + 1).
			 ] ifFalse: [ 
			(clet = 3) ifTrue: [ 
				cp:= (cp + 1)
				 ].
			clet:= 1.
			plet:= let.
			 ].
		start:= false.
		 ] ifFalse: [ 
			(let = $ ) ifTrue: [ 
				start:= true.	
			  ].
		 ].
	i:= (i+1).
	 ].

(clet = 3) ifTrue: [ 
	cp:= cp + 1.
	 ].

Transcript show: 'The amount of times that 3 consecutive words start with the same letter is: ', cp asString; cr.
```
