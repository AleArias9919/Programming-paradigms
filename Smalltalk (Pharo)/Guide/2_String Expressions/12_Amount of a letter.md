### Dado un texto terminado en ‘/’ se pide determinar cuántas veces aparece determinada letra, leída de teclado. 

```smalltalk
| s1 clet let |

s1:= (UIManager default request: 'Enter a text: ').
clet:= 0.
Transcript clear.
Transcript show: 'Text: ', s1; cr.

let:= (UIManager default request: 'Enter a letter: ') first.

s1 do: [ :i |
	(i = let) ifTrue: [ 
		clet:= (clet + 1)
		 ].
	 ].

Transcript show: 'Cantidad de veces que aparece la letra -', let asString, '-: ', clet asString.


```
