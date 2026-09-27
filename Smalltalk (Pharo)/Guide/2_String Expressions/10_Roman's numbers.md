### Escribir un subprograma que dado n, lea n caracteres que forman un número romano y que devuelva un string que represente a dicho número romano y un número que represente el equivalente decimal. 

```smalltalk
| n x dec c y |.

n:= (UIManager default request: 'Enter the number of Romans characters: ') asNumber.

Transcript clear.

x:= Array new: n.
y:= Array new: n.

1 to: n do: [  :i|
	x at: i put: ((UIManager default request: 'Enter character: ') first) asUppercase.
	 ].

dec:= 0.
c:= 0.

1 to: n do: [ :k|
	
	((x at: k) = $I) ifTrue: [ 
		y at: k put: 1.
		 ].
	
	((x at: k) = $V) ifTrue: [ 
		y at: k put: 5.
		 ].
	
	((x at: k) = $X) ifTrue: [ 
		y at: k put: 10.
		 ].
	
	((x at: k) = $L) ifTrue: [ 
		y at: k put: 50.
		 ].
	
	((x at: k) = $C) ifTrue: [ 
		y at: k put: 100.
		 ].
	
	((x at: k) = $D) ifTrue: [ 
		y at: k put: 500.
		 ].
	
	((x at: k) = $M) ifTrue: [ 
		y at: k put: 1000.
		 ].
	 ].

1 to: n do: [ : j|
	(j = n) ifTrue: [ 
		dec:= dec + (y at: j)
		 ] ifFalse: [ 
			((y at: j) < (y at: (j+1))) ifTrue: [ 
				dec:= dec - (y at: j).
				] ifFalse: [ 
				dec:= dec + (y at: j).
				 ].
		 ].
	 ].

Transcript show: 'Roman number entered: ', x asString; cr.
Transcript show: 'Decimal number: ', dec asString; cr.
```
