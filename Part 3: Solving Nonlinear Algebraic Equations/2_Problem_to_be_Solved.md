##  Description of the problem considered in this tutorial section

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mass-action ion-exchange equilibrium is used as an example problem in this tutorial part. The total amount present of each ionic species (m<sub>A</sub>, ...) is specified along with the volumes of the mobile (or liquid) phase (V<sub>m</sub>) and resin phase (V<sub>r</sub>) for the case where three (or more) ions are present (i.e., ions A, B, C etc.). Then, the liquid phase composition (c<sub>A</sub>, ...) and the resin-phase composition (q<sub>A</sub>, ...) are determined by solving a system of nonlinear algebraic equations. The ion-exchange equilibrium reactions for the case of three ionic species are as follows (where the subscripts r and m denote the resin and mobile phases, respectively):

<span style="font-family:Consolas; font-size:1em;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;z<sub>A</sub> (B<sub>r</sub>) +  z<sub>B</sub> (A<sub>m</sub>) &nbsp;<font size="4">&harr;</font>&nbsp;z<sub>A</sub> (B<sub>m</sub>) + z<sub>B</sub> (A<sub>r</sub>)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;z<sub>A</sub> (C<sub>r</sub>) +  z<sub>C</sub> (A<sub>m</sub>) &nbsp;<font size="4">&harr;</font>&nbsp;z<sub>A</sub> (C<sub>m</sub>) + z<sub>C</sub> (A<sub>r</sub>)
</span>

In order to more easily generize this development to any number of ions, integers will be used for the various ions such that A=1, B=2, and C=3 etc. The equations to solve for the case of three ionic species are therefore (when given in residual form): 

<span style="font-family:Consolas; font-size:1em;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = K<sub>21</sub> - (q<sub>2</sub>/c<sub>2</sub>)<sup>z<sub>1</sub></sup> * (c<sub>1</sub>/q<sub>1</sub>)<sup>z<sub>2</sub></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = K<sub>31</sub> - (q<sub>3</sub>/c<sub>3</sub>)<sup>z<sub>1</sub></sup> * (c<sub>1</sub>/q<sub>1</sub>)<sup>z<sub>3</sub></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = Q - z<sub>3</sub>*q<sub>3</sub> - z<sub>2</sub>*q<sub>2</sub> - z<sub>3</sub>*q<sub>3</sub><br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = m<sub>1</sub> -  c<sub>1</sub>*V<sub>m</sub> - q<sub>1</sub>*V<sub>r</sub><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = m<sub>2</sub> -  c<sub>2</sub>*V<sub>m</sub> - q<sub>2</sub>*V<sub>r</sub><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 = m<sub>3</sub> -  c<sub>3</sub>*V<sub>m</sub> - q<sub>3</sub>*V<sub>r</sub><br>
</span>

where:     
<span style="font-family:Consolas; font-size:1em;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;z<sub>1</sub>, z<sub>2</sub>, z<sub>3</sub> are the ionic charges<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c<sub>1</sub>, c<sub>2</sub>, c<sub>3</sub> are the mobile-phase (i.e., liquid-phase) ion concentrations in mM<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;q<sub>1</sub>, q<sub>2</sub>, q<sub>3</sub> are the stationary-phase (i.e., adsorbed-phase or resin-phase ion concentrations) in mM<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;m<sub>1</sub>, m<sub>2</sub>, m<sub>3</sub> are the total amounts present of each ion in millimoles<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;K<sub>21</sub> is the ion-exchange selectivity coefficient of ion 2 with respect to ion 1<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;K<sub>31</sub> is the ion-exchange selectivity coefficient of ion 3 with respect to ion 1<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Q is the ion-exchange total capacity of the resin in milli-equiv./liter<br>
</span>

Note that K<sub>21</sub> and K<sub>31</sub> are dimensionless and that K<sub>11</sub> is unity by definition and is not present in the above equations.

###  Further details of this problem are given in:

1.  P. Wankat, Separation Process Engineering, 4th Ed., Section 19.5.1, Pearson, 2007.  
2.  J.D. Seader, E.J. Henley, D.K. Roper, Separation Process Principles, 3rd Ed., Chpt. 15, Wiley, 2011.  
3.  G. Klein, "Calculation of ideal or empirically modified mass-action equilibria in heterovalent, multicomponent ion exchange," Computers and Chemical Engineering, 8, 171-178, 1984.
