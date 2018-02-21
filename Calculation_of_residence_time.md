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

```
