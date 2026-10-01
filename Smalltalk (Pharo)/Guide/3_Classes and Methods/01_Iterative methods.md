###  Métodos Iterativos o estructuras de control. Recordar la diferencia entre cada uno de ellos y verificar 
cada trozo de código, en caso de error corregirlo y explicar que sucede. (Prestar atención a las 
variables de bloque).


a. | suma  cont| 
suma:=0. 
cont:=1. 
[cont<11]whileTrue:[suma:=suma+cont. 
cont:=cont+1]. 
^suma 
b. |a| 
a:=0. 
6 timesRepeat:[a:=a+2]. 
^a 
c. |x| 
x:=0. 
1 to:5 do:[:i| x:=x+i]. 
^x  
d. | cad| 
cad:='Paradigmas de Programación'. 
1 to:(cad size) by:2 do:[:i| cad at:i put:$-]. 
^cad 
e. | x| 
x:='Paradigmas de Programación'. 
(x size) timesRepeat:[:i| x at:i put:$-]. 
^x
