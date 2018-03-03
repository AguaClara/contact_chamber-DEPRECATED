#Coagulant and Clay Stock Concentration Calculations
Calculates the concentration of clay and coagulant in the plant
given the stock concentrations

##Coagulant Stock Concentration

```python
from aide_design.play import*

coag_stock = 70.9 * u.grams / u.liters
coag_vol = (10 * u.milliliter).to(u.liter)
water_vol = 5 * u.liter

c_coag = (coag_stock * coag_vol)/(water_vol)

q_coag = 5 * u.milliliter/u.min #Flow rate of coagulant from stock solution
q_plant = 180 * u.milliliter/u.min  #Flow rate in sed tank
q_plant.to(u.milliliter/u.sec)

c_plant = (q_coag * c_coag/q_plant).to(u.mg/u.liter)
#we should try to make this 1.5 mg/L
```

#Calculate coagulant stock concentrations
```python
c_plant = 1.5 * u.milligram/u.liter
q_plant = 180 * u.milliliter/u.min
q_coag = 5 * u.milliliter/u.min
c_coag = (c_plant*q_plant)/q_coag
water_vol = 5 * u.liter
coag_stock = 70.9 * u.grams / u.liters

coag_vol = (c_coag*water_vol)/coag_stock
(coag_vol).to(u.milliliter)

```

#Clay stock concentration
```python
from aide_design.play import*

clay_mass = 3 * u.grams
water_vol2 = 5 * u.liter

c_clay = clay_mass/water_vol2
q_clay = 4
q_plant2 = 5

c_plant = q_clay * c_clay/q_plant2

c_plant

```
