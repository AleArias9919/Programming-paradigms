### Dos números se dicen amigos cuando uno de ellos es igual a la suma de todos los divisores del otro excepto el mismo. Ejemplo: los números 220 (1+2+4+5+10+11+20+22+44+55+110=284) y 284 (1+2+4+71+142=220) son amigos. 
### Escriba un método booleano que permita discernir si dos números (parámetros) son amigos.

```smalltalk

| x y i j sx sy |.

Transcript clear.

x:= (UIManager default request: 'Enter the first number' ) asNumber.
y:= (UIManager default request: 'Enter the second number' ) asNumber.

i:=1.
sx:= 0.
sy:= 0.

[ i < x ] whileTrue: [ 
	((x % i)=0) ifTrue: [ 
		sx:= sx + i.
		 ].
	i:= i + 1.
	 ].

i:= 1.

[ i < y ] whileTrue: [ 
	((y % i)=0) ifTrue: [ 
		sy:= sy + i.
		 ].
	i:= i + 1.
	 ].

(sx = y and: [sy = x]) ifTrue: [ 
	Transcript show: 'The numbers ', x asString, ' and ', y asString, ' are amicable numbers.'; cr.
	 ] ifFalse: [ 
		Transcript show: 'The numbers ', x asString, ' and ', y asString, ' are NOT amicable numbers.'; cr.	
	 ]

```
