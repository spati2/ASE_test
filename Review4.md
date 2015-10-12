[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner1.png">](https://github.com/txt/mase/blob/master/README.md)   
[At a glance...](https://github.com/txt/mase/blob/master/OVERVIEW.md) |
[Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) |
[Models](https://github.com/txt/mase/blob/master/MODELS.md) |
[Code](https://github.com/txt/mase/tree/master/src) |
[Lecturer](http://menzies.us) 


### Simulated Annealing

  1. In a few lines, define ordered and unordered search. In what way are they different?
  
  Ordered-search; e.g. the tree and graph searchers discussed below. In this kind of search, the solutions spreads out in a wave over over some solution space.

Unordered-search where a partial solution is quickly (?randomly) generated, then maybe fiddled with. A common unordered search method is to generate a number of slots, each with random values as done in PSO or simulated annealing or MAXWALKSAT.

  2. In a few lines, compare and contrast: (1) Greedy search; (2) Local Search; and (3) Stochastic search. What, if any, are the trade-offs in using a Stochastic search?
  
A greedy algorithm is an algorithm that follows the problem solving heuristic of making the locally optimal choice at each stage[1] with the hope of finding a global optimum. In many problems, a greedy strategy does not in general produce an optimal solution, but nonetheless a greedy heuristic may yield locally optimal solutions that approximate a global optimal solution in a reasonable time.

local search is a metaheuristic method for solving computationally hard optimization problems. Local search can be used on problems that can be formulated as finding a solution maximizing a criterion among a number of candidate solutions. Local search algorithms move from solution to solution in the space of candidate solutions (the search space) by applying local changes, until a solution deemed optimal is found or a time bound is elapsed.

Stochastic search is a form of unordered search where we make use of fast processors to explore a number of possibilities very quickly.

  3. In about 10 lines, write down the pseudo-code for SA. Number each line.
  
 ''' Code
  s = s0;e = E0;
  sb = s0;eb = E0;
  k = 0
  while k<kmax and e<emax:
    sn = neighbor(s)
    en = Energy(sn)
    IF en<eb Then 
      eb = en;sb = sn
      print "!"
    FI
    IF en<e Then 
      e = en;s = sn
      print "+"
    FI
    IF P(e,en,(1-k/kmax))<e Then 
      e = en;s = sn
      print "?"
    FI
    print "."
    k = k+1
    if k%50==0 Then print "sb\n"
return sb

Let s = s0
let sb = s0
For k = 0 through kmax (exclusive):
T ← temperature(k ∕ kmax)
Pick a random neighbour, snew ← neighbour(s)
If E(snew)<E(sb), move to best state:
sb <-snew
If E(snew)<E(s), move to local best state:
s <-snew
If P(E(s), E(snew), T) ≥ random(0, 1), move to the new state:
s ← snew
Output: the final state s
'''

  4. In the pseudo-code for SA, you used a neighbourhood function `Neighbour()`. Write down an expression for this.
  

  5. 4. In the pseudo-code for SA, you used a probability function `P(e_new, e_old, t)`. What would be a valid mathematical expression for this?
  
    P(e_new, e_old, t) = e^((old-new)/t).

  6. With respect to function `P(e_new, e_old, t)`, justify the following statements:
      * Initially, SA is like a drunk, then it sobers up
      
        The function is calculated as P(e_new, e_old, t) = e^((old-new)/t).
        For cases where new<old and for larger values of t, we will  be making jumps to higher energy states. This is termed as the "drunk" state. With each step of the annealing schedule, we reduce t. As a result the value of P will increase and the annealer makes lesser jumps to higher energy states. This stage is termed as "sobering" up.
      
      * SA consumes lower memory.
      
        At each stage of the SA we store 3 solutions:- the energy of the current state, the energy of the local best energy and the global best energy.

  7. How would you terminate a stochastic algorithms such as SA sooner? (*HINT: Look at variances of epochs*)
  
  
  8. When finding a solution, you can either mutate towards ''Heaven'' (A better spot) or you can choose to mutate away from "Hell" (A worse spot). Why would you choose one over the other? (*HINT: One of them has a better diversity of search.*)


_________

<img align=right src="https://raw.githubusercontent.com/txt/mase/master/img/pd-icon.png">Copyright © 2015 [Tim Menzies](http://menzies.us).
This is free and unencumbered software released into the public domain.   
For more details, see the [license](https://github.com/txt/mase/blob/master/LICENSE.md).

