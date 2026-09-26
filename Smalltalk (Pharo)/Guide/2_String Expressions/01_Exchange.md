### Dada una cadena de entrada, devolver otra en la que los caracteres en mayúsculas hayan sido cambiados por caracteres en minúsculas y viceversa. 

```smalltalk
| s1 s2 |

Transcript clear.

s1:= (UIManager default request: 'Enter a string: ') asString.

Transcript show: 'Original string: ', s1; cr.
Transcript show: 'Inverted: '.


s1 do: [ : x |
	(x isUppercase) ifTrue:[
		Transcript show: x asLowercase.
		] ifFalse: [ 
		Transcript show: x asUppercase.
		 ]
	 ].
```
