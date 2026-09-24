### Escribir un programa que ingrese un listado de números e informe la cantidad de múltiplos de 2, 3, 5 y 7. 

```smalltalk
| x c2 c3 c5 c7 i arr aux|

Transcript clear.

arr:= (UIManager default request: 'Enter the amount of numbers in the array: ') asNumber. 

x:= Array new: arr.
c2:=0.
c3:=0.
c5:=0.
c7:=0.

i:= 1.

[ i <= arr ] whileTrue: [ 
	aux:= (UIManager default request: 'Enter the value of the position ', i asString, ' of the array') asNumber.
	x at: i put: aux.
	i:= (i + 1).
	 ].

i:= 1.


[ i <= arr ] whileTrue: [ 
	(((x at: i)%2)=0) ifTrue: [ 
		c2:= c2+1
		 ].
	(((x at: i)%3)=0) ifTrue: [ 
		c3:= c3+1
		 ].
	(((x at: i)%5)=0) ifTrue: [ 
		c5:= c5+1
		 ].
	(((x at: i)%7)=0) ifTrue: [ 
		c7:= c7+1
		 ].
	
	i:= i + 1
	 ].

i:= 1.

Transcript show: 'Amount of multiples of 2: ', c2 asString; cr.

Transcript show: 'Amount of multiples of 3: ', c3 asString; cr.

Transcript show: 'Amount of multiples of 5: ', c5 asString; cr.

Transcript show: 'Amount of multiples of 7: ', c7 asString; cr.


```
