---
tags:
cssclasses:
  - Major
---
The Laplace transform is used to analyze a more diverse set of ODE's, such as non-linear and piecewise ODE's, defined by the function below:
$$\mathcal{L}\{f(t)\}=\int_0^{\infty}e^{-st}f(t)dt$$
Using the [[Linear Functions|linear properties]] of the Laplace function, we can algebraically separate terms in the Laplace domain into common forms to perform the inverse, thus allowing the application of the Laplace to more complex ODE's. This algebraic manipulation allows us to obtain the solution in terms of algebraic and step functions. A table of common Laplace Transforms are shown below:

| $f(x)$             | $\mathcal{L}\{f(x)\}=F(s)$                                                         |
| ------------------ | ---------------------------------------------------------------------------------- |
| $t^n$              | $\frac{n!}{s^{n+1}}$                                                               |
| $sin(kt)$          | $\frac{k}{s^2+k^2}$                                                                |
| $cos(kt)$          | $\frac{s}{s^2+k^2}$                                                                |
| $f^{(n)}(t)$       | $s^nF(s)-s^{n-1}f(0)-s^{n-2}f^{(1)}(0)-\cdot\cdot\cdot-sf^{(n-2)}(0)-f^{(n-1)}(0)$ |
| $u_nf(t)$          | $e^{-ns}\mathcal{L}\{f(t+n)\}$                                                     |
| $u_nf(t-n)$        | $e^{-ns}F(s)$                                                                      |
| $e^af(t)$          | $F(s-a)$                                                                           |
| $t^nf(t)$          | $(-1)^n\frac{d^n}{ds^n}F(s)$                                                       |
| $\frac{f(t)}{t}$   | $\int_s^\infty F(\sigma)d\sigma$                                                   |
| $\frac{sin(t)}{t}$ | $\frac{\pi}{2}-arctan(s)$                                                          |
