### Convertir un número en el sistema decimal al sistema binario. 

```smalltalk
| x b r |.

Transcript clear.

x:= (UIManager default request: 'Enter a decimal number: ') asNumber.

b:= 0.

Transcript show: 'Number in decimal: ', x asString; cr.

[ (0 < x) ] whileTrue: [ 
	r:= (x % 2).
	b:= ((b*10) + r).
	x:= x//2.
	 ].

Transcript show: 'The number in binary is: ', b asString.
```
