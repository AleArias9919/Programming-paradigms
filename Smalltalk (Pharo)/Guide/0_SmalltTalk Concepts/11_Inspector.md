#### Smalltalk has a window called "inspector" that allows you to view and modify an object's instance varibales. Evaluate this code and say what you can observe. (ST tiene una ventana llamada “Inspector” que permite ver y cambiar las variables de instancia de un objeto. Evalúa este código y di qué observas.)

#### Solution:
```smalltalk
| a |
a := { 1. 2. #sam. 'joe'. { 4. 5 } }.
a at: 2 put: 3 / 4.
a inspect

Result: {1. (3/4). #sam. 'joe'. #(4 5)}

Note: In this version of Pharo, literal arrays created with #(...) are read-only and cannot be modified with at:put:. To create a modifiable array, use {...} instead.
```




