```python
"""Calculates the concentration of clay and coagulant in the plant
given the stock concentrations"""

from aide_design.play import*

#Coagulant stock concentration
coag_stock = 70.9 * u.grams / u.liters
coag_vol = (10 * u.milliliter).to(u.liter)
water_vol = 5 * u.liter

c_coag = (coag_stock * coag_vol)/(water_vol)

q_coag = 5 * u.milliliter/u.min #Flow rate of coagulant from stock solution
q_plant = 180 * u.milliliter/u.min  #Flow rate in sed tank

c_plant = q_coag * c_coag/q_plant

#Clay stock concentration
clay_mass = 3 * u.grams
water_vol2 = 5 * u.liter

c_clay = clay_mass/water_vol2
q_clay =
q_plant2 =

c_plant = q_clay * c_clay/q_plant2
```
