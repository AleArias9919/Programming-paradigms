### Se tiene un arreglo de n números naturales que se quiere ordenar por frecuencia, y en caso de igual frecuencia, por su valor. 
#### Por ejemplo, a partir del arreglo [1, 3, 1, 7, 2, 7, 1, 7, 3] se quiere obtener [1, 1, 1, 7, 7, 7, 3, 3, 2]. 

```smalltalk
| x1 x2 c n tot may lmay j2|

Transcript clear.

c:= (UIManager default request: 'Enter the number of elements of the array') asNumber.

x1:= Array new: c.
x2:= Array new: c.

Transcript show: 'Original array: ['.

1 to: c do: [ : i |
    x1 at: i put: (UIManager default request: 'Enter the value of the position ', i asString, ' of the array (Natural number): ') asNumber.
	Transcript show: (x1 at: i).
    ].

Transcript show: ']'.

may:= 0.

1 to: c do: [ :i2 |
	x2 at: i2 put: -1.
	 ].

[ (x2 at: c) = -1 ] whileTrue: [ 
	1 to: c do: [ : j |
		tot:= 0.
	   	n:= (x1 at: j).
		(n = -1) ifFalse: [ 
		1 to: c do: [ : k |
			(n = (x1 at: k)) ifTrue: [ 
				tot:= (tot + 1).
			 ].
			(may < tot) ifTrue: [ 
			may:= tot.
			lmay:= n.
		 	].
		].
	].

	1 to: c do: [ : m|
		j2:= 1.
		[ j2 <= may ] whileTrue: 
			[((x2 at: m) = -1) ifTrue: [ 
				x2 at: m put: lmay.
				j2:= (j2+1).
				 ].
				((x1 at: m) = lmay) ifTrue:[
					x1 at: m put: -1. ]
				ifFalse: [ 
			
				 ].
			 ] 
		].
	].
]
```
