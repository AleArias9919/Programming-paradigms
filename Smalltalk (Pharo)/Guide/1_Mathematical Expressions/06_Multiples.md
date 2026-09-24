### Dado un número determinar sus múltiplos. 

```smalltalk
| n i j c|

Transcript clear.

n:= (UIManager default request: 'Enter a number: ') asNumber.
j:= (UIManager default request: 'Enter the number of multiples wanted: ') asNumber.
i:= 1.

[j >= i] whileTrue: [ 
	c:= (n * i).
	Transcript show: 'The number multiplied by ', i asString , ' is: ', c asString; cr.
	i:= i + 1
	 ]

```
