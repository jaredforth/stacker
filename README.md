# stacker

A simple domain specific language in Racket. This is part of the excellent book [Beautiful Racket](https://beautifulracket.com/stacker), which I would highly recommend checking out. 

## Usage 

The entire language definition is in `stacker.rkt`, so to use create a new file with:

```
#lang reader "stacker.rkt"
```

You can then add integers and addition and multiplication operators like:

```
5
8
+
6
*
```
