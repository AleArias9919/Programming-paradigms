## Clase 14-10-2026  y 15-10-2026 

####  Comparación de frases utilizando un método matemático. 
##### | arr1 arr2 resultado|
##### arr1:= #(1 2 3 4) 
##### arr2:=#(5 6 7 8) 
##### resultado := arr1 productoEscalar: arr2. 
##### resultado := arr1 productoEscalar: arr2 longitud:3. 

### a) Método: productoEscalar: unArreglo.
```smalltalk
| productoE | 

"Controlar contenido del arreglo" 

productoE:=0. 

self size = unArreglo size ifTrue:[ 
		1 to: self size do:[:i| 
			productoE:= productoE + ((self at: i) * (unArreglo at:i)). 
			]]. 

^productoE 
```
### sol1>

```smalltalk
<img width="746" height="352" alt="{2CC0112F-4D5F-4D55-81EA-675F6C861320}" src="https://github.com/user-attachments/assets/a4a5b3df-09f1-4871-b682-6611f92a943b" />
<img width="729" height="397" alt="{60FC4178-E128-4E15-90EF-3C63C54523D4}" src="https://github.com/user-attachments/assets/547a8933-42f8-4654-9512-bc7f0a701fa2" />
<img width="414" height="236" alt="{9F644488-E412-4E0A-8832-3CBA94322489}" src="https://github.com/user-attachments/assets/63ba5512-c12b-465c-96a2-ee27f21a518b" />
<img width="560" height="473" alt="{10328BF8-607E-4163-8333-DDB120B192D8}" src="https://github.com/user-attachments/assets/fa24138a-a72d-4fcc-8c89-2f96b5930171" />

```

### Sol2:
#### Métodos:
```smalltalk

construirVector: frase 
	"Dado un arreglo se retornara un vector de la posicion " 
|vector| 
vector:= Array new: (self size). 

1 to: (self size) do:[:i| 
(frase includes: (self at: i)) 
	ifTrue:[ vector at: i put: 1] 

	ifFalse: [ vector at: i put: 0 ]. 

	]. 

^vector

====================================================  

prodEscalar: vect 
	"Se ingresa dos Vectores y se realiza el producto escalar, retornando el resultado un entero" 
	| acum | 

 

	acum:= 0. 

	1 to: (self size) do: [ :i| 

		acum:= acum +((self at: i)*(vect at: i)) 

		]. 

	^acum. 

===================================================== 

```



### Sol1:

```smalltalk


```


### Sol1:




### Sol2:

```smalltalk


```
###
