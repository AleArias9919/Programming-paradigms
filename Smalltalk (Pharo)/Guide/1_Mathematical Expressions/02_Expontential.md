# Realizar x^y. 

```smalltalk
| x y c |.

Transcript clear.

x:= (UIManager default request: 'Enter the base: ') asNumber.
y:= (UIManager default request: 'Enter de exponent: ') asNumber.
c:= x.

Transcript show: x asString, ' raised to ', y asString, ': '.

[ y > 1 ] whileTrue: [ 
	
	c:= (c * x).
	y:= (y - 1).
	 ].

Transcript show: c asString.
```
