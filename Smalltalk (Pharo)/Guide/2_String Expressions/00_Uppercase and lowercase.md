### Convertir una cadena a mayúsculas y minúsculas.

```smalltalk
| s1 s2 s3 |.

Transcript clear.

s1:= (UIManager default request: 'Enter a string: ') asString.

s2:= s1 asUppercase.
s3:= s1 asLowercase.

Transcript show: 'Original string: ', s1; cr.
Transcript show: 'Uppercase: ', s2; cr.
Transcript show: 'Lowercase: ', s3; cr.
```
