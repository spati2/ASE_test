[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner1.png">](https://github.com/txt/mase/blob/master/README.md)   
[At a glance...](https://github.com/txt/mase/blob/master/OVERVIEW.md) |
[Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) |
[Models](https://github.com/txt/mase/blob/master/MODELS.md) |
[Code](https://github.com/txt/mase/tree/master/src) |
[Lecturer](http://menzies.us) 


What is the problem with local maxima?

1. In the following diagram, each square has the same x,y,z axis. What might the names of those x,y,z values?
![](https://github.com/timm/sbse14/wiki/etc/img/landscape/WrightFitness.jpg)

body weight, fur thickness, and lifespan 


2. Explain the following, using the above diagram:

 * Holes:- Holes are the regions of minima on a landscape. A minima is a region that has values less than that of its neighbours.
 
 * Poles:- Poles are the regions of maxima on a landscape. A minima is a region that has values less than that of its neighbours.
 
 * Saddles:- Saddles are the precarious flat regions between a Hole and a Pole. Tread carefully.
 
 * Local minima:- A minima is a region that has values less than that of its neighbours.
 * Flat:- Flat is region is a landscape where the value doesnt change. No local maxima or minima
 * Brittle:- brittleness are solutions that are not robust, meaning that any perturbations to your solution space will result in much worse solutions. So the solutions that are "...even better solution that is surrounded by a set of far less fit solutions."


3. Explain the following term and describe how it handles the problem of flat: Retries.

4. How does the following techniques avoid the problems of local maxima?

  Simulated annealing
    - Retries
    - Momentum (make sure you explain momentum)
  
5. Local search can be characterized as follows

   + Jump all around the hills
   + Sometimes, sitting still while rolling marbles left and right
   + Then taking one step along the direction where the marbles roll the furthest.
   + Go to 1.

In the following code snippet, explain where you'd find 5.
```
FOR i = 1 to max-tries DO
  solution = random assignment
  FOR j =1 to max-changes DO
    IF  score(solution) > threshold
        THEN  RETURN solution
    FI
    c = random part of solution 
    IF    p < random()
    THEN  change a random setting in c
    ELSE  change setting in c that maximizes score(solution) 
    FI
RETURN failure, best solution found
```


_________

<img align=right src="https://raw.githubusercontent.com/txt/mase/master/img/pd-icon.png">Copyright © 2015 [Tim Menzies](http://menzies.us).
This is free and unencumbered software released into the public domain.   
For more details, see the [license](https://github.com/txt/mase/blob/master/LICENSE.md).

