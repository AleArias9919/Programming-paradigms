### Idem anterior, decir si es par o impar.

```smalltalk
| n j it |

Transcript clear.

j:= 0.
it:= (UIManager default request: 'Enter amount of numbers ') asNumber.

[ j < it ] whileTrue: [ 
	"THE SOLUTION STARTS HERE: "
	
	n:= (UIManager default request: 'Enter a number: ') asNumber.
	
	((n % 2) = 0) ifTrue: [ 
		Transcript show: 'The number ', n asString, ' is an even number'; cr.
		 ] ifFalse: [ 
		Transcript show: 'The number ', n asString, ' is an odd number'; cr.
		 ].
	"END"

j:= j + 1.
	 ].

```

