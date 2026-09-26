### Se tiene un arreglo de n números naturales que se quiere ordenar por frecuencia, y en caso de igual frecuencia, por su valor. 
#### Por ejemplo, a partir del arreglo [1, 3, 1, 7, 2, 7, 1, 7, 3] se quiere obtener [1, 1, 1, 7, 7, 7, 3, 3, 2]. 

```smalltalk
| x c n tot |

Transcript clear.

c:= (UIManager default request: 'Enter the number of elements of the array') asNumber.

x:= Array new: c.

1 to: c do: [ : i |
    x at: i put: (UIManager default request: 'Enter the value of the position ', i asString, ' of the array (Natural number): ') asNumber.
    ].

1 to: c do: [ : j |
    n:= (x at: j).
    tot:= 0.
    1 to: c do: [ : k |
        ((x at: k) = n) ifTrue: [
            tot:= (tot + 1).
				x at: k put: -1.
            ].
        ].
	(n ~= -1) ifTrue: [ 
    Transcript show: 'The amount of times that the number ', n asString, ' appears is: ', tot asString; cr.
  ]
]

```
