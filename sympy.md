# SymPy

↑ **Parent:** [Computer algebra system](computer-algebra-system.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SymPy)

This is the dream [cheating](exam.md) software every student should know about.

It also has serious applications obviously. [https://www.sympy.org/scipy-2017-codegen-tutorial/](https://www.sympy.org/scipy-2017-codegen-tutorial/) mentions [code generation](automatic-programming.md) capabilities, which sounds super cool!

The code in this section was tested on `sympy==1.8` and [Python](python-programming-language.md) 3.9.5.

Let's start with some basics. [fractions](fraction.md):
```
from sympy import *
sympify(2)/3 + sympify(1)/2
```
outputs:
```
7/6
```
Note that this is an exact value, it does not get converted to [floating-point numbers](floating-point-number.md) where precision could be lost!

We can also do everything with symbols:
```
from sympy import *
x, y = symbols('x y')
expr = x/3 + y/2
print(expr)
```
outputs:
```
x/3 + y/2
```
We can now evaluate that expression object at any time:
```
expr.subs({x: 1, y: 2})
```
outputs:
```
4/3
```

How about a square root?
```
x = sqrt(2)
print(x)
```
outputs:
```
sqrt(2)
```
so we understand that the value was kept without simplification. And of course:
```
sqrt(2)**2
```
outputs `2`. Also:
```
sqrt(-1)
```
outputs:
```
I
```
`I` is the [imaginary unit](imaginary-unit.md). We can use that symbol directly as well, e.g.:
```
I*I
```
gives:
```
-1
```

Let's do some trigonometry:
```
cos(pi)
```
gives:
```
-1
```
and:
```
cos(pi/4)
```
gives:
```
sqrt(2)/2
```
The exponential also works:
```
exp(I*pi)
```
gives;
```
-1
```

Now for some [calculus](calculus-split.md). To find the [derivative](derivative.md) of the [natural logarithm](natural-logarithm.md):
```
from sympy import *
x = symbols('x')
print(diff(ln(x), x))
```
outputs:
```
1/x
```
Just read that. One over x. Beauty. And now for some integration:
```
print(integrate(1/x, x))
```
outputs:
```
log(x)
```
OK.

Let's do some more. Let's solve a simple [differential equation](differential-equation.md):
```
y''(t) - 2y'(t) + y(t) = sin(t)
```
Doing:
```
from sympy import *
x = symbols('x')
f, g = symbols('f g', cls=Function)
diffeq = Eq(f(x).diff(x, x) - 2*f(x).diff(x) + f(x), sin(x)**4)
print(dsolve(diffeq, f(x)))
```
outputs:
```
Eq(f(x), (C1 + C2*x)*exp(x) + cos(x)/2)
```
which means:

$$
f(x) = C_1 + C_2x e^x + cos(x)/2
$$

To be fair though, it can't do anything crazy, it likely just goes over known patterns that it has solvers for, e.g. if we change it to:
```
diffeq = Eq(f(x).diff(x, x)**2 + f(x), 0)
```
it just blows up:
```
NotImplementedError: solve: Cannot solve f(x) + Derivative(f(x), (x, 2))**2
```
Sad.

Let's try some [polynomial equations](algebraic-equation.md):
```
from sympy import *
x, a, b, c = symbols('x a b c d e f')
eq = Eq(a*x**2 + b*x + c, 0)
sol = solveset(eq, x)
print(sol)
```
which outputs:
```
FiniteSet(-b/(2*a) - sqrt(-4*a*c + b**2)/(2*a), -b/(2*a) + sqrt(-4*a*c + b**2)/(2*a))
```
which is a not amazingly nice version of the [quadratic formula](quadratic-formula.md). Let's evaluate with some specific constants after the fact:
```
sol.subs({a: 1, b: 2, c: 3})
```
which outputs
```
FiniteSet(-1 + sqrt(2)*I, -1 - sqrt(2)*I)
```
Let's see if it handles the [quartic equation](quartic-equation.md):
```
x, a, b, c, d, e, f = symbols('x a b c d e f')
eq = Eq(e*x**4 + d*x**3 + c*x**2 + b*x + a, 0)
solveset(eq, x)
```
Something comes out. It takes up the entire terminal. Naughty. And now let's try to [mess with it](abel-ruffini-theorem.md):
```
x, a, b, c, d, e, f = symbols('x a b c d e f')
eq = Eq(f*x**5 + e*x**4 + d*x**3 + c*x**2 + b*x + a, 0)
solveset(eq, x)
```
and this time it spits out something more magic:
```
ConditionSet(x, Eq(a + b*x + c*x**2 + d*x**3 + e*x**4 + f*x**5, 0), Complexes)
```
Oh well.

Let's try some [linear algebra](linear-algebra-split.md).
```
m = Matrix([[1, 2], [3, 4]])
```
Let's invert it:
```
m**-1
```
outputs:
```
Matrix([
[ -2,    1],
[3/2, -1/2]])
```

**Table of contents**

- [SymPy special function](sympy-special-function.md)
  - [python/sympy\_cheat/logarithm\_integral.py](_file/python/sympy_cheat/logarithm_integral.py.md)

## ↑ Ancestors (11)

1. [Computer algebra system](computer-algebra-system.md)
2. [Computer algebra](computer-algebra.md)
3. [Numerical software](numerical-software.md)
4. [Scientific software](scientific-software.md)
5. [Scientific computing](scientific-computing.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Logarithmic integral function](logarithmic-integral-function.md)
- [Sylvester's law of inertia](sylvester-s-law-of-inertia.md)
