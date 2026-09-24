### Solicitar el ingreso de un nº y verificar si este es o no primo.

```smalltalk

| x n i j it|

Transcript clear.

it:= (UIManager default request: 'Enter amount of numbers ') asNumber.

j:= 0.

[ j < it ] whileTrue: [ 
	n:= (UIManager default request: 'Enter a number: ') asNumber.
	i:= 2.
	x:= 0.

[i < n] whileTrue: [ 
	((n % i) = 0) ifTrue: [ 
		x:= x + 1.
		 ].
	i:= i + 1
	 ].

(x = 0) ifTrue: [ 
	Transcript show: 'The number ', n asString, ' is a cousin number'; cr.
	 ] ifFalse: [
	Transcript show: 'The number ', n asString, ' is not a cousin number'; cr.
		].

j:= j + 1.
	 ].

```
