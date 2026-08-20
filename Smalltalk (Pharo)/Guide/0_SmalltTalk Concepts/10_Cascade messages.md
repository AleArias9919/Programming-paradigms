#### Cascade messages, this is what we call a set of messages sent to the same object. Check these two expressions and explain the difference (Mensajes en cascada, llamamos así al conjunto de mensajes que enviamos a un mismo objeto. 
Verifica estas dos expresiones y explica la diferencia).

As we already know, in Pharo, everything is an object, and every action is performed by sending messages to those objects. A message is simply a request for an object to perform an operation or return a value.

When we need to send several messages to the same object, we can use cascade messages. This allows us to chain multiple operations on the same object without having to repeat its name each time, making the code more concise and readable.

The key theory needed to understand cascades is:

Each message in a cascade is sent to the same receiver, regardless of what it returns.
The syntax uses a semicolon ; to separate the messages.
The final value of the entire cascade expression is the original receiver object, not the result of the last message.


#### a)
```smalltalk
3 factorial; factorial; factorial 

Result: 6

Notes: -factorial is sent to the original object (3) at each step.
       -Each factorial is evaluated independently on 3.
       -The final value of the entire expression is the original receiver object, that is, 3.

Summary: a cascade executes the messages sequentially, but always on the same object, ignoring intermediate results.
```


#### b)
```smalltalk
3 factorial factorial factorial 

Result: 26012189435657951002049032270810436111915218750169457857275418378508356311569473822406785779... (continuous)

Each message is applied to the result of the previous message:
-3 factorial → 6
-6 factorial → 720
-720 factorial → a very large number
Summary: the messages are applied cumulatively to the previous results.

Caution — Key difference:
-With ; (cascade) → all messages are sent to the original object.
-Without ; → each message is applied to the result of the previous message, producing cumulative effects.
```


