```python
from aide_design.play import*
rho = 1000 * (u.kilogram/u.m ** 3)
L = (25.4 * u.cm).to(u.m)
t = 90 * u.s
u = L/t
mu = 0.000890 * (u.kilogram/(u.m * u.s))
re = (rho*u*L)/mu


```
