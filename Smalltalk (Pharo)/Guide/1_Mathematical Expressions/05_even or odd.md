### Idem anterior, decir si es par o impar.

```smalltalk
| n j |

Transcript clear.

j:= 0.
it:= (UIManager default request: 'Enter amount of numbers ') asNumber.

	
n:= (UIManager default request: 'Enter a number: ') asNumber.
	
((n % 2) = 0) ifTrue: [ 
	Transcript show: 'The number ', n asString, ' is an even number'; cr.
	] ifFalse: [ 
	Transcript show: 'The number ', n asString, ' is an odd number'; cr.
		 ].
```

