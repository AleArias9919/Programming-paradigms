###  Ingresar dos cadenas y devolver una 3º que contenga los elementos de las 2 anteriores pero intercalados.

```smalltalk
| s1 s2 s3 i |.

Transcript clear.

s1:= (UIManager default request: 'Enter the first string: ').
s2:= (UIManager default request: 'Enter the second string; ').

s3:= ''.

i:= 1.

[ (i <= s1 size) and: (i <= s2 size) ] whileTrue: [ 
	s3:= s3, (s1 at: i) asString.
	s3:= s3, (s2 at: i) asString.
	i:= i + 1.
	  ].

Transcript show: 'First string: ', s1; cr.
Transcript show: 'Second string: ', s2; cr.


((s1 size) < (s2 size)) ifTrue: [ 
	i to: (s2 size) do: [ : j |
		s3:= s3, (s2 at: j) asString.
		 ].
	 ] ifFalse: [ 
	i to: (s1 size) do: [ :k|
		s3:= s3, (s1 at: k) asString.
		 ].
	 ].

Transcript show: 'Mixed string: ', s3; cr.
```
