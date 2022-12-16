# stacker

A simple domain specific language in Racket. This is part of the excellent book [Beautiful Racket](https://beautifulracket.com/stacker), which I would highly recommend checking out. 

## Usage 

The entire language definition is in `stacker.rkt`, so to use create a new file with:

```racket
#lang reader "stacker.rkt"
```

You can then add integers and addition and multiplication operators like:

```racket
5
8
+
6
*
```

### Functional Rewrite 

The program was rewritten in a functional paradigm in `funstacker` which can be used in the same way:

```racket
#lang reader "stacker.rkt"

5
8
+
6
*
```

### Stackerizer

`stackerizer` is a program that converts `stacker` code into S-expresssions and can be used:

```racket
#lang s-exp "stackerizer.rkt"

(* 1 2 (+ 3 4 (* 5 6 (+ 7 8 (* 9 10)))))
``` 

This will create `stacker` code like:

```racket
8
+
7
+
6
*
5
*
4
+
3
+
2
*
1
*
```
