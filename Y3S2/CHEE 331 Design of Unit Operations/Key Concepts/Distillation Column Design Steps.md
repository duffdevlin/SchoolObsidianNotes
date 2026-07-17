---
tags:
cssclasses:
  - WIP
---
When designing a distillation column, the complex nature of optimizing the system requires multiple "passes" to obtain a near optimal configuration. Following each of these sets of steps sequentially will allow you to determine a good starting point for further sets, or alternatively determine if the process is not economically or technically feasible before the more time-consuming detailed design processes are done.
# Rough Hand Design (Binary System)
1. For binary systems, obtain the [[Phase Diagrams|x,y phase diagram]] of the components with the mole fractions representing the more volatile component. Using the desired purity, find the [[Flash Drum|bottoms]] and [[Flash Drum|distillate]] flow rates using an [[Distillation External Balance|external balance]].
2. On the [[Phase Diagrams|x,y phase diagram]], plot the [[Distillation Column Formulas|feed line]] by finding the [[Feed Quality|feed quality]], then from the points along the y=x line corresponding to the desired [[Flash Drum|bottoms]] and [[Flash Drum|distillate]] compositions, connect them to the intersection of the [[Distillation Column Formulas|feed line]] and the [[Phase Diagrams|equilibrium line]]. Using an estimated slope from the [[Distillation Column Formulas|top operating line]], find the minimum [[Reflux Ratio|reflux ratio]], $R_{min}$.
3. Using a value between 1.1-1.5 times the value of $R_{min}$, find the number of [[Distillation Column Trays|trays]] required by plotting the [[Distillation Column Formulas|top]] and [[Distillation Column Formulas|bottom operating lines]], and [[Distillation Column Formulas|feed line]] onto a new [[Phase Diagrams|x,y phase diagram]] based on feed quality and the new reflux ratio. Move horizontally from the point on the y=x line corresponding to the desired [[Flash Drum|distillate]] composition until you reach the [[Phase Diagrams|equilibrium line]], then moving down vertically until you reach the [[Distillation Column Formulas|top operating line]]. Continue this pattern, extending vertically past the [[Distillation Column Formulas|top operating line]] instead going until the [[Distillation Column Formulas|bottom operating line]] after you reach the point these lines intersect with the [[Distillation Column Formulas|feed line]]. Continue until you reach or extend beyond the desired [[Flash Drum|bottoms]] composition.
4. Calculate the fractional stage number by calculating what fraction of the last horizontal line is required to reach the desired [[Flash Drum|bottoms]] composition. Add this to the number of complete boxes drawn on the [[Phase Diagrams|x,y phase diagram]] to obtain the required number of trays. As one of these trays is the reboiler and has a separate efficiency take one away from this total number before applying an estimated [[Tray Efficiency|tray efficiency]], typically estimated at 0.6. Dividing the number of trays given by the boxes by the [[Tray Efficiency|tray efficiency]] gives us a rough estimate for necessary [[Distillation Column Trays|distillation trays]]. 
5. Calculate the necessary duties in the [[Reboiler|reboiler]] and [[Condenser|condenser]], assuming the enthalpy and heat capacity of each component is defined by the dominant component in each stream. The [[Condenser|condenser]] should operate [[Process Assumptions|isothermally]] and only take into account the [[Thermodynamic Properties|latent heat of vaporization]], while the reboiler needs to raise the temperature 3-5 degrees above the boiling point, requiring taking into account [[Thermodynamic Properties|latent]] and [[Thermodynamic Properties|sensible heat]].
6. Iterate through the range of 1.1-1.5$R_{min}$ until a balance is found between a reasonable number of [[Distillation Column Trays|trays]], and the calculated duty required in the [[Condenser|condenser]] and [[Reboiler|reboiler]]. [^2]
# Rough Computer-Aided Design (HYSYS)
1. Select a fluid package that uses [[Equations of State|equations of state]] that are best suited for the chemicals you intend to separate. For multicomponent systems, select your [[Distillation Key Components|light]], and [[Distillation Key Components|heavy key]] components based on the compounds with most similar volatility that require separation. Using [[Distillation External Balance|external balances]], find the [[Flash Drum|distillate]] and [[Flash Drum|bottoms]] flow rates based on recovery of two compounds for multicomponent systems, or purity for binary systems.
2. 
**Write out steps and then fine tune order/expand**
- ~~Fluid package selection~~
- ~~Use external balances to find flow rates~~
- Select tray spacing between 6-36 inches, number of trays, and enter stage efficiency
- Page 878 of textbook gives some info
- Find suitable pressure at top and bottom of column, assuming 3-4 inches of liquid mixture pressure increase per tray going down
- Find optimal feed stage, graphically optimizing to find a minimum absolute value of re-boiling and condensing duties[^1]
- Find column diameter using standard sizes based on calculated reflux ratio in HYSYS
- Find capital cost of distillation column and reboiler and condenser, annualize based on project lifecycle and add operational cost
- plot various numbers of trays and optimize total annual cost graphically
- Explore variations in feed rates effect on weeping/flooding/entrainment and adjust design accordingly

[^1]: Due to [[Thermodynamic Properties|enthalpy]] being a state property, the difference between the re-boiling and condensing duties remains constant, making only finding the minimum of one of the values required for finding the most economically optimized feed stage.

[^2]: A reasonable number of trays should be somewhere between 5-20, but may be outside these bounds given by the difficulty of separating the desired compounds.
