---
tags:
cssclasses:
  - Major
---
Given a non-homogeneous ODE that can't be solved by the [[Method of Undetermined Coefficients|method of undetermined coefficients]], and has [[Complementary ODE Solutions|complementary solutions]] $y_1$, and $y_2$, the [[Non-Homogeneous ODE Solutions|non-homogeneous solution]] can be shown below:
$$y_{NH}=y_2\int\frac{y_1f(t)}{W(y_1,y_2)}dt-y_1\int\frac{y_2f(t)}{W(y_1,y_2)}dt$$
Where the function, $f(t)$, is the [[Ordinary Differential Equations|forcing function]], and $W(y_1,y_2)$ is the [[Wronskian]] of the [[Complementary ODE Solutions|complementary solutions]], $y_1$, and $y_2$.