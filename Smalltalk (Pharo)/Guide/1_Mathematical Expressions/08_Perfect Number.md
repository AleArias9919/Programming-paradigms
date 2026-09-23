### Un número entero positivo se dice perfecto si es igual a la suma de todos sus divisores, excepto el mismo. 
#### Ejemplo: los números 6 (1+2+3), 28 (1+2+4+7+14) y 496 (1+2+4+8+16+31+62+124+248) son perfectos. 
#### Escriba un método booleano que permita diferenciar si un número (único parámetro) es perfecto. 


```smalltalk
| i x y s |.

x:= (UIManager default request: 'Enter a number: ') asNumber.

s:= 0.
i:=1.

[i < x] whileTrue: [ 
	((x % i) = 0) ifTrue: [ 
		s:= s + i ].
	i:= i + 1 
	].

(s = x) ifTrue: [ 
	Transcript show: 'Es un número perfecto' 
	]
	ifFalse: [ 
		Transcript show: 'No es un número perfecto'
		 ].

Transcript cr.

```
