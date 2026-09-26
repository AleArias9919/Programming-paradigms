### Dada una cadena de entrada, devolver otra en la cual las palabras estén en formato ‘tipo título’. 

```smalltalk
| s1 s2 space |

Transcript clear.

s1:= (UIManager default request: 'Enter a string: ').
s2:= ''.

space:= true.

s1 do: [ : i| 
	(i = $ ) ifTrue: [ 
		s2:= s2, i asString.
		space:= true
		 ] ifFalse: [ 
		(space) ifTrue: [ 
			s2:= s2, (i asUppercase) asString.
			space:= false.
			 ] ifFalse: [ 
			s2:= s2, (i asLowercase) asString.
			 ].
		].
	 ].

Transcript show: 'The original string is: ', s1; cr.
Transcript show: 'The new string is: ', s2; cr.
```
