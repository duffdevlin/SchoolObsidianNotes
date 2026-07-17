---
cssclasses:
  - Major
---
Material balances looks at the mass in a system. Since mass is conserved, we can either deal with mass as a whole, or the mass of individual components. When dealing with individual chemical components, it is sometimes useful to deal in [[Stoichiometry|moles]] of each component, which would just be a conversion using molar mass. From the most basic level all mass balances are in the form below:
$$\frac{dm}{dt}=Input-Output+Generation-Consumption$$
When dealing with non-reactive species, you only need to deal with the [[Material Balance Input|input]] and [[Material Balance Output|output]] terms on the right side of the balance. Ignoring the intricacies of reactive systems, whether using [[Kinetic Models|reaction kinetics]], or [[Scaling Lab Data|test data and imperial assumptions]], will make this balance much easier to analyze. A similar removal of the [[Material Balance Consumption|consumption]] and [[Material Balance Generation|generation]] terms is done when analyzing the mass of the system as a whole, as the conservation of mass dictates that the transformation of one species to another will keep the overall mass constant.

An analog which removes the [[Material Balance Input|input]] and [[Material Balance Output|output]] terms of a system, leaving the [[Material Balance Generation|generation]] and [[Material Balance Consumption|consumption]] consumption terms behind, is the assumption of a [[Batch Reactor|batch process]]. Since a [[Batch Reactor|batch process]] does not have any mass flowing into or out of it, when evaluating the mass balance of all species combined, $\frac{dm}{dt}$ goes to zero.

When looking at any system, another useful tool to evaluate them is the [[Process Assumptions|assumption]] of [[Steady-State Solutions|steady-state]], leading to the simplified balance below:
$$Input+Generation=Output+Consumption$$
While simple processes may be able to be solved by analyzing the [[Degrees of Freedom|degrees of freedom]] when evaluating different systems within, this is a very rough method of solving that does not tend to be the most time efficient process. More [[CHEE 222 Process Dynamics and Numerical Methods|advanced techniques]] may be used to evaluate these systems in a more robust manner, allowing you to model processes in real time, and evaluate processes that may have more than one [[Steady-State Solutions|steady state]] solution.
