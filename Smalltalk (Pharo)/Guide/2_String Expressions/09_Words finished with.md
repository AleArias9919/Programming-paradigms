### Ídem anterior, pero contar la cantidad de palabras que terminan con una letra determinada. Dado un texto, se pide: 
#### i. La posición inicial de la palabra más larga, 
#### ii. La lontitud del texto.
#### iii. Cuantas palabras con una longitud entre 8 y 16 caracteres poseen más de tres veces la vocal ‘a’.

```smalltalk
| s1 cp ca let s2 cp2 pos maypos mayp start j|.

Transcript clear.

s1:= (UIManager default request: 'Enter a text: ').
let:= (UIManager default request: 'Enter a letter: ') first.

Transcript show: 'Text: ', s1; cr.
Transcript show: 'Size: ', (s1 size) asString; cr.

s1:= s1 asLowercase.
s1:= s1, ' '.

start:= true.
s2:= ''.

j:= 1.
mayp:= 0.
cp2:= 0.
cp:= 0.

s1 do: [ :i|
	(start) ifTrue: [ 
		pos:= j.
		s2:= s2, i asString.
		start:= false.
		 ] ifFalse: [ 
			(i = $ ) ifTrue:[
				start:= true.
				((s2 size) > mayp) ifTrue: [ 
					mayp:= (s2 size).
					maypos:= (pos)
					 ].
				(((s2 size) >=8) and: ((s2 size) <= 16 )) ifTrue: [ 
					ca:= 0.
					s2 do: [ :k |
						(k = $a) ifTrue: [ 
							ca:= ca + 1
						 ].
					 ].
				(ca > 3) ifTrue: [ 
					cp2:= cp2 + 1 ]
				 ].
			(let = (s2 at: (s2 size))) ifTrue: [ 
				cp:= cp + 1.
				 ].
			s2:= ''.
			 ] ifFalse: [
			s2:= s2, i asString.
			].
		 ].
	j:= (j + 1).
].

Transcript show: 'Initial position of the longest word: ', maypos asString; cr.
Transcript show: 'Number of words between 8 and 16 characters that have more than 3 times the letter -a-: ', cp2 asString; cr.

Transcript show: 'Number of words finished with the letter -', let asString, '-: ', cp asString;cr. 
```
