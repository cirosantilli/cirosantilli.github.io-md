# Robin boundary condition

↑ **Parent:** [Neumann boundary condition](neumann-boundary-condition.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Robin_boundary_condition)

Linear combination of a [Dirichlet boundary condition](dirichlet-boundary-condition.md) and [Neumann boundary condition](neumann-boundary-condition.md) at each point of the boundary.

Examples:
- [heat equation](heat-equation.md) when metal plaque is immersed in a large external environment of fixed temperature.

  In this case, the normal derivative at the boundary is proportional to the difference between the temperature of the boundary and the fixed temperature of the external environment.

  The result as time tends to infinity is that the temperature of the plaque tends to that of the environment.

  Shown a solved example in the [FreeFem](freefem.md) tutorial: [https://doc.freefem.org/tutorials/thermalConduction.html](https://doc.freefem.org/tutorials/thermalConduction.html) ([https://github.com/FreeFem/FreeFem-doc/blob/1d5996d8b891fd553fd318321249c2c30f693fc3/source/tutorials/thermalConduction.rst)](https://github.com/FreeFem/FreeFem-doc/blob/1d5996d8b891fd553fd318321249c2c30f693fc3/source/tutorials/thermalConduction.rst))

## ↑ Ancestors (7)

1. [Neumann boundary condition](neumann-boundary-condition.md)
2. [Boundary condition](boundary-condition.md)
3. [Differential equation](differential-equation.md)
4. [Calculus](calculus-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)
