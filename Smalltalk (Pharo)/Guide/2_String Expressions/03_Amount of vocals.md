### Contar la cantidad de vocales de una frase. 

```smalltalk
| s1 cv |

Transcript clear.

s1:= (UIManager default request: 'Enter a phrase: ').

cv:= 0. 

s1:= s1 asUppercase.

s1 do: [ :i | 
	((i = $A) or: ((i = $E) or: ((i = $I) or: ((i = $O) or: (i = $U))))) ifTrue: [ 
		cv:= cv + 1
		 ] 
	 ].

Transcript show: 'The amount of vocals of the phrase -', s1, '- is: ', cv asString.

```
