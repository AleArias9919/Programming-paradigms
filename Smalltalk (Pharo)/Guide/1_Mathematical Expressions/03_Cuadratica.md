### Solicitar al usuario que ingrese los coeficientes de una ecuación cuadrática, calcular sus raíces y mostrarlas. 

```smalltalk
| a b c r1 r2 |

Transcript clear.

a:= (UIManager default request: 'Enter the cuadratic coefficient: ') asNumber.
b:= (UIManager default request: 'Enter the lineal coefficient: ') asNumber.
c:= (UIManager default request: 'Enter the independent number: ') asNumber.

r1:= (b negated + ((b raisedTo: 2)-(4*a*c)) sqrt) / (2*a).

r2:= (b negated - ((b raisedTo: 2)-(4*a*c)) sqrt) / (2*a).

Transcript show: 'Equation: ', a asString, 'x^2 + ', b asString, 'x + ', c asString; cr. 
Transcript show: 'Roots: r1 = ', r1 asString, ', r2 = ', r2 asString.
```
