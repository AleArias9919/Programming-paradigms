###  Dado un texto terminado en punto, determinar cuál es la vocal que aparece con mayor frecuencia.

```smalltalk
| s1 cv x may mayf |

s1:= (UIManager default request: 'Enter a text finished with a dot: ').

Transcript clear.

Transcript show: 'Text: ', s1; cr.

s1:= s1 asLowercase.

x:= Array new: 5.

1 to: 5 do: [ :k |
	x at: k put: 0 asNumber.
	].

s1 do: [ :i |
	(i = $a) ifTrue:[
		x at: 1 put: ((x at: 1) + 1).
	 ].

	(i = $e) ifTrue:[
		x at: 2 put: ((x at: 2) + 1).
	 ].

	(i = $i) ifTrue:[
		x at: 3 put: ((x at: 3) + 1).
	 ].

	(i = $o) ifTrue:[
		x at: 4 put: ((x at: 4) + 1).
	 ].

	(i = $u) ifTrue:[
		x at: 5 put: ((x at: 5) + 1).
	 ].
].

may:= 0.

1 to: 5 do: [ : j|
	(may < (x at: j)) ifTrue: [ 
		may:= (x at: j).
		(j = 1) ifTrue: [ 
			mayf:= 'a'.
			 ] ifFalse: [ 
			(j = 2) ifTrue: [ 
				mayf:= 'e'.
				 ] ifFalse: [ 
				(j = 3) ifTrue: [ 
					mayf:= 'i'
					 ] ifFalse: [ 
					(j = 4) ifTrue: [ 
						mayf:= 'o'.
						 ] ifFalse: [ 
						mayf:= 'u'.
						 ]
					 ]
				 ]
			 ]
		 ] 
	 ].

Transcript show: 'The vocal which appears most frequently is: ', mayf; cr.
```
