#Residence Time Calculation

```python
#calculates the residence time of coagulant in contact chamber given the upflow velocity in the sedimentation tube

from aide_design.play import*
upflowv= 2 * u.millimeter / u.s
diameter= 1 * u.inch
Area= pc.area_circle(diameter)
flowrate= (upflowv * Area).to(u.mL/u.s)
flowrate
DiameterCC=diameter
LengthCC= 10 * u.inch
VolumeCC= pc.area_circle(DiameterCC)*LengthCC
residencet=(VolumeCC/flowrate).to(u.s)

residencet
```
#Required RPM for Water Pump to Achieve Required Volumetric Flow
```python

WaterPump_rpm = ((SedTube_Flow/0.8)*(60*(u.s))).magnitude

print('The required RPMs for the water pump to achive a flow rate of 1.52 mL/s is ' +ut.sig(WaterPump_rpm,4)+' RPM.')

```                                                                                

#Experiment Flow Rates
```python
Sixteen_RPM_Conversion = 0.8 #mL/revolution
WaterSpeed = 76 #revolutions per minute
Q_Water = (WaterSpeed * Sixteen_RPM_Conversion)*(u.mL/u.min)
print('The flow of water into the system is ' +ut.sig(Q_Water,4)+ '.')

Coag_Speed = 10 #RPM
Q_Stock = (YB_RPM_Conversion * Coag_Speed)*(u.mL/u.min)
print('The flow of coagulant into the system is ' +ut.sig(Q_Stock,4)+ '.')

Clay_Speed = 16 #Approximate pump speed - variable
Q_Clay = (YB_RPM_Conversion * Clay_Speed)*(u.mL/u.min)
print('The flow of clay solution into the system is ' +ut.sig(Q_Clay,4)+ '.')

Plant_Flow = Q_Water + Q_Stock + Q_Clay
print('The total flow rate through the system is ' +ut.sig(Plant_Flow,4)+ '.')                                                                               
```

#Coagulant Concentration through system
```python

#15RPM for Coagulant Pump, 76 RPM Water
StockCoag_Conc = (0.2836/4) * (u.g/u.L) #Coaglant flowing from stock
TotalSystem_Flow = 64.67 * (u.mL/u.min) #Raw Water + Clay + Coagulant
Q_coag = 1.49* (u.mL/u.min)
C_plant= ((Q_coag*StockCoag_Conc)/TotalSystem_Flow).to(u.mg/u.L)
print('The coagulant concentration throughout the system in this trial is ' +ut.sig(C_plant,4)+ '.')

```
