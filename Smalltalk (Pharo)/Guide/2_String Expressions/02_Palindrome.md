### Verificar si una frase es un palíndromo o no. 

```smalltalk
| s1 s2 x |

Transcript clear.

s1:= s1 asLowercase.

s2:= s1 reversed.

(s1 = s2) ifTrue: [ 
	Transcript show: '-', s1, '- is a palindrome'; cr.
	 ] ifFalse: [ 
	Transcript show: '-', s1, '- is not palindrome'; cr.
	 ].
```
