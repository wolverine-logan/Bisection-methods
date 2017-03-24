Bisection method
Instructions
1. Use Python3
2. Use any editor of your choice (eg: Atom) to implement the Algorithm
3. Run your Implementation against the given Test Equations
4. Research and provide additional Test Equations
5. Push the Code and Test Output on Github
6. Publish the link on Moodle
Aim
Implementation of the Bisection Algorithm in Python .
Background
The Bisection method is a simple root finding Algorithm. The root is found by
successivly halving the search space for the root until the root is found.
The Algorithm
1. Choose two initial end points a and b such that f (a) and f (b) have the
opposite sign. This ensures that the root is inbetween a and b.
2. Estimate the new root c with
a + b
c =
2
3. Calculate the function value at the midpoint, f (c) . Check If f (c) is sufficiently
close to 0.IF YES then the Bisection has converged and c is the root of the
function. Print the root and exit.
IF NO the Bisection has not converged. Replace the value of a with c if
the root is inbetween c and b, otherwise replace the value of b with c if
the root lies inbetween a and c.
4. Loop back to step 2
Pseudocode
The Pseudocode for Bisection according to Wikipedia.
INPUT: Function f, endpoint values a, b, tolerance TOL, maximum iterations NMAX
CONDITIONS: a < b, either f(a) < 0 and f(b) > 0 or f(a) > 0 and f(b) < 0
OUTPUT: value which differs from a root of f(x)=0 by less than TOL
 
N ← 1
While N ≤ NMAX # limit iterations to prevent infinite loop
  c ← (a + b)/2 # new midpoint
  If f(c) = 0 or (b – a)/2 < TOL then # solution found
    Output(c)
    Stop
  EndIf
  N ← N + 1 # increment step counter
  If sign(f(c)) = sign(f(a)) then a ← c else b ← c # new interval
EndWhile
Output("Method failed.") # max number of steps exceeded
Assignment
1. Implement the Bisection method in Python
2. Find the roots for the following equations:
i.
x
2
− 5x − 7 = 0
ii.
x
Reference
3
+ 8x = 0https://en.wikipedia.org/wiki/Bisection_method
