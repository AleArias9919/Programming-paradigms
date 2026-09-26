#### Realizar un algoritmo que lea una serie de números reales y verifique si están ordenados ascendentemente o no, informando por pantalla.

```smalltalk
| x n act tf |.

Transcript clear.

n:= (UIManager default request: 'Enter the amount of elements of the array: ') asNumber.

Transcript show: 'Array: [ '.

x:= Array new: n.

tf:= true.

1 to: n do: [ :i |
	 x at: i put: (UIManager default request: 'Enter the value of the position', i asString, ' of the array' ) asNumber.
	Transcript show: (x at: i) asString, ' '.
	 ].

Transcript show: ']'; cr.


1 to: (n - 1) do: [ :j |
 	act:= (x at: j).
	(act > (x at: (j + 1))) ifTrue: [ 
		tf:= false.
		 ].
	 ].

(tf = true) ifTrue: [ 
	Transcript show: 'The array is sorted in ascending order'.
	 ] ifFalse: [ 
	Transcript show: 'The array is not sorted in ascending order'.
	 ].

```
