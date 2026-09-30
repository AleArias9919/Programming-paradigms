### 1) Realizar la conversión de grados sexagesimales a radian. Considere el ingreso de grados a convertir en el formato: grados, minutos y segundos, por ejemplo: 127° 15’ 26’’ El resultado a mostrar, redondeado a 4 decimales, siguiendo el ejemplo, sería: 2,2211 rad En el caso de que el grado ingresado no sea bien formado (escrito correctamente) devolver nil. 
```smalltalk
| s1 g m s i mb grados rad |

s1:= (UIManager default request: 'Ingrese un ángulo en formato ggg mm ss: ').

Transcript clear.
g:= ''.
m:= ''.
s:= ''.
mb:= 0.

i:= 1.
[ (s1 at: i) ~= $° ] whileTrue: [ 
	g:= g, (s1 at: i) asString.
	i:= i + 1.
	mb:= mb+1
	 ].

i:= i+1.

[ (s1 at: i) ~= $` ] whileTrue: [ 
	m:= m, (s1 at: i) asString.
	i:= i + 1.
	 ].

i:= i+1.

[ ((s1 at: i) = $` and: ((s1 at: (i+1)) = $`)) not] whileTrue: [ 
	s:= s, (s1 at: i) asString.
	i:= i + 1.
	 ].

Transcript show: 'Angle: ', g, '°',  m, '`', s, '``'.

g:= g asNumber.
m:= m asNumber.
s:= s asNumber.

grados:= (g + (m/60) + (s/3600)).

rad:= grados * (Float pi / 180).

rad:= (rad * 10000) rounded / 10000.0.


Transcript show: 'Radianes: ', rad asString.
```

### 2) Calcule la serie alternada de Gregory-Leibniz: 
<img width="147" height="93" alt="{F6FCBB8F-4ADE-45B0-9DAE-BF166BD93227}" src="https://github.com/user-attachments/assets/ca9281ad-6fb1-4eb6-bcd1-d5f4498be2b3" />

#### Nota: analizar si es posible optimizar el cálculo de cada término.   

```smalltalk
| k result sign prec term |.

Transcript clear.

k := 1.
result := 0.
sign := 1.
prec := 0.0001.

term := sign / ((2*k)-1).

[ term abs >= prec ] whileTrue: [
    term := (sign / (2 * k - 1)).
    result := result + term.
    k := k + 1.
    sign := (sign * (-1))
].

Transcript show: 'The result of the series is: ', (result asFloat) asString; cr.
```
