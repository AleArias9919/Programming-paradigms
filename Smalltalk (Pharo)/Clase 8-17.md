Hacer sumatoria de 1/n! hasta que el número sea menor o igual a 10 raised to: -9

```smalltalk
| n c termino |

n := 1.
c := 0.
termino := 1 / n factorial.

[ termino > (10 raisedTo: -9) ] whileTrue: [
    c:= c + termino.
    n := n + 1.
    termino := 1 / n factorial.
].

Transcript Show: c
```
