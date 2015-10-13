[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner1.png">](https://github.com/txt/mase/blob/master/README.md)   
[At a glance...](https://github.com/txt/mase/blob/master/OVERVIEW.md) |
[Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) |
[Models](https://github.com/txt/mase/blob/master/MODELS.md) |
[Code](https://github.com/txt/mase/tree/master/src) |
[Lecturer](http://menzies.us) 


# Review 7: Differential Evolution

- Explain: 
- DE's build new examples by extrapolating between known ones.
  * Pick three point points (X,Y,Z)
  * New = X + f * (Y - Z)
- Explain the following DE constants:
- What is np and how is it used?
  * Candidates from population
- What is cf and how is it used?
  * cros over factor. probability to pick cross over 
- What is f and how is it used?
  * extrapolating factor
- Write down, in 10 lines or less, pseudo-code for DE. <br>
```
  Let x be agent in the population, n is the dimension of the problem, cf is cross over factor, f is extrapolate factor
  Initialize all agents X with random positions in the search-space.
  Until a termination criterion is met (e.g. number of iterations performed, or adequate fitness reached), repeat the following:
    For each agent x in the X do:
     Pick three agents a,b, and c from the population at random, they must be distinct from each other as well as from agent x
     if random_num is less than cf:
      create new candidate a + f(b-c)
     else:
       a as new candidate, for some randomisation
     if new candidate better than x:
      update x,total score
    return total, X
```
- Distinguish between the following two kinds of DE algorithms:
    + DE/rand/1
      * Storn denotes DE variants as DE/selection/extrapolations. For example, the above DE is actually DE/rand/1;
        - We extrapolate from some candidate X, chosen at random.
        - We only add in values from one other extrapolation
    + DE/best/2
      * It uses two extrapolations, but based on the best X seen so far:
        - Xbest + F * (A + B - Y - Z)
        - Here, A,B,Y,Z are candidates selected at random

_________

<img align=right src="https://raw.githubusercontent.com/txt/mase/master/img/pd-icon.png">Copyright © 2015 [Tim Menzies](http://menzies.us).
This is free and unencumbered software released into the public domain.   
For more details, see the [license](https://github.com/txt/mase/blob/master/LICENSE.md).

