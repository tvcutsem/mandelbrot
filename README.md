# mandelbrot

Renders the famous [Mandelbrot fractal](https://en.wikipedia.org/wiki/Mandelbrot_set) in parallel using multiple CPU cores, using the `java.util.concurrent` [Fork/Join](https://docs.oracle.com/javase/tutorial/essential/concurrency/forkjoin.html) framework.

Compile:

```
javac Mandelbrot.java
```

To render sequentially:

```
java Mandelbrot
```

To render in parallel:

```
java Mandelbrot -p
```

To show a grid of pixel areas allocated to each leaf task (showing what pixels can get calculated in parallel):

```
java Mandelbrot -p -g
```

Result:

![Rendered result](output.png)

This code was originally written as part of my university course on [Multicore Programming](http://soft.vub.ac.be/~tvcutsem/multicore/) to show students a typical example of parallel speedup through the Fork/Join abstraction.