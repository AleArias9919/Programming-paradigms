### Realizar  las operaciones F/G y F*G. Utilizando sumas y restas sas

```smalltalk

| x y d p may men r i j|

Transcript clear.



i:= (UIManager default request: 'Enter number of iterations: ') asNumber.
j:= 1.

[ i > 0 ] whileTrue: [ 


Transcript show: '---------------------Iteration ', j asString, '----------------------------'; cr.

x:= (UIManager default request: 'Enter the first number: ') asNumber.
y:= (UIManager default request: 'Enter the second number: ') asNumber.

d:= 0.
p:= 0.

Transcript show: 'For x = ', x asString, ' and y = ', y asString, ': '; cr.

(x > y) ifTrue: [ 
	may:= x.
	men:= y.
	 ] ifFalse: [ 
	may:= y. 
	men:= x.
	 ].

r:= may.

[ r > men ] whileTrue: [ 
	d:= (d + 1).
	r:= (r - men).
	 ].

Transcript show: 'The division is: ', d asString; cr.

[ men > 0 ] whileTrue: [ 
	p := (p + may).
	men:= (men - 1). 
	 ].


Transcript show: 'The product is: ', p asString; cr.
Transcript cr.
Transcript cr.

i:= i - 1.
j:= j + 1.
	]

```
