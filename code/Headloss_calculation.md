#Headloss across Flocculator

Calculates the headloss due to pressure difference across the coiled flocculator using the Darcy–Weisbach equation.

```python
from aide_design.play import*

p1 = 253.1714 * u.kilogram / (u.m * u.s**2)
p2 = 235.9223 * u.kilogram / (u.m * u.s**2)

rho = 1000 * u.kilogram / u.meter**3
g = 9.81 * u.m/u.sec**2

headloss = (p2-p1)/(rho*g)



```
