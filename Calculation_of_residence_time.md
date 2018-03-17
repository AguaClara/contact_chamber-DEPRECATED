```python
from aide_design.play import*
upflowv= 2 * u.millimeter / u.s
tankdiameter= 1 * u.inch
Areatank= pc.area_circle(tankdiameter)
flowrate= (upflowv * Areatank).to(u.mL/u.s)
flowrate
DiameterCC= 3 * u.inch
LengthCC= 10 * u.inch
Area= pc.area_circle(DiameterCC)
VolumeCC= (Area*LengthCC).to(u.mL)
residencet=(VolumeCC/flowrate).to(u.s)
residencet
```
