###  Existen clases definidas en ST que permiten visualizar distintos tipos de ventanas solicitando información al usuario o informando al mismo. Evalúa estas expresiones. 
#### 1. UIManager default request: '¿Cuál es tu edad ? '  
#### 2. |nombre| nombre:=UIManager default request:'¿Cómo te llamas? '. 
#### ^UIManager inform: 'Hola ', (nombre asString). 
##### c. |resp| 
-resp:= UIManager confirm:'Hoy es tu cumpleaños??'. 
-resp ifTrue:[UIManager inform:'FELIZ CUMPLE!!'] 
