### Calcular la raiz cubica de N aplicando el método Newton - Raphson:
<img width="300" height="156" alt="image" src="https://github.com/user-attachments/assets/ddfedcb5-2e4f-4af1-906a-ed9c64055a9a" />

#### xn = valor próximo al número N.	precisión p = 0.000001 
#### Ejemplo: N=11	xn = 2 entonces xn+1 = (1/2)*(2 + 5/2) y así sucesivamente, hasta la precisión deseada. En cada iteración se utiliza el nuevo valor de xn+i calculado.

```smalltalk
| result N prec x1 x2|.

N:= (UIManager default request: 'Enter the number: ') asNumber.
prec:= 0.000001.

Transcript clear.

x1:= 2.
x2:= (1/3) * ((2 * x1) + (N / (x1 raisedTo: 2))).

[ (x2-x1) abs > prec ] whileTrue: [ 
	x1:= x2.
	x2:= ((1/3) * ((2 * x1) + (N / (x1 raisedTo: 2))))
	
	 ].

Transcript show: 'Result: ', (x2 asFloat) asString.

```
