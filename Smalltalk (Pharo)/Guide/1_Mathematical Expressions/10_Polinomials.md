### Ingresar 2 polinomios y realizar la suma y el producto de ambos.

```smalltalk
| g1 g2 x1 x2 x3 i may j |
 
Transcript clear.

g1:= (UIManager default request: 'Enter the grade of the first polinomial: ') asNumber. 
g2:= (UIManager default request: 'Enter the grade of the second polinomial: ') asNumber.

x1:= Array new: g1. x2:= Array new: g2.

( g1 > g2 ) ifTrue: [ 
	may:= g1.
	 ] ifFalse: [ 
	may:= g2 
	].

x3:= Array new: may.

i:= 1.

[ i <= g1 ] whileTrue: [ 
	x1 at: i put: (UIManager default request: 'Enter the value of the position ', i asString, ' of the array: ') asNumber.
	i:= (i + 1).
	 ].

i:= 1.

[ i <= g2 ] whileTrue: [ 
	x2 at: i put: (UIManager default request: 'Enter the value of the position ', i asString, ' of the array: ') asNumber.
	i:= (i + 1).
	 ].

i:= may.
j:= 1.
Transcript show: 'Result: '.

[ i > 0 ] whileTrue: [ 
	x3 at: i put: ((x1 at: i) + (x2 at: i)).
	
	i:= i - 1.
	 ].
	
i:= may.

[ may >= j ] whileTrue: [ 
	Transcript show: ' + ', (x3 at: j) asString, 'x^', (i-1) asString.
	j:= j + 1
	]

```
