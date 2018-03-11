# Contact Chamber, Spring 2018
#### Cheer Tsang, Yeonjin Yun, Canaan Delgado
#### March 9, 2018

## Abstract
Briefly summarize your previous work, goals and objectives, what you have accomplished, and future work. (100 words max)

## Introduction
Explain how the completion of your challenge will affect AguaClara and the mission of providing safe drinking water (or sustainable wastewater treatment!). If this is a continuing team, how will your contribution build upon previous research? What needs to be further discovered or defined? If this is a new team, what prompted the inclusion of this team?

## Literature Review and Previous Work
Coagulation is the process by which smaller particles collide and adhere to each other to make larger, more dense particles known as flocs. This process is generally introduced before the filtration process to allow maximum aid in removing solid sediments in water. In the late 1940’s, a new theory was developed that distinguished two modes of removal of colloidal impurities. This process has been widely known to be cost-effective and has revolutionized the water treatment process (Balik and Aydin, 2015).

The process known as double layer compression describes the overcoming of the repulsive forces between the particles to adhere together and precipitate. This process would later be later known as coagulation (Jiang, 2015). Stable particles of clay and organic substances found in influent raw water are negatively charged, causing particles to repel each other and remain suspended in solution. As positively charged coagulant is added to the water, the negative charges are neutralized, allowing the particles to adhere together into aggregations called “microflocs."

The coagulants that are normally used for wastewater treatment tend to be predominantly inorganic salts of aluminum or iron, alum in particular being the most ubiquitous. When these coagulants are introduced to water, the aluminum ions have a tendency to hydrolyze in an unstable manner, eventually forming “a range of metal hydrolysis species.” AguaClara plants utilize, polyaluminum chloride (PACl), a more commercially available polymeric aluminum coagulant.

In a study of coagulation kinetics, batch experiments were conducted to examine the different ways that PACl and alum destabilize particles and the different factors that affect how quickly particles are destabilized. At low temperatures, the already hydrolyzed PACl can be advantageous over the traditional coagulants because temperature fluctuation has less of an impact on the coagulant efficacy. Since previous research showed that the rate of collisions between particles is slower than the rate of particle destabilization, particle destabilization is the rate-determining step. Therefore, the efficiency of the coagulation process depends on the rate of particle destabilization, and as a result, optimizing the particle destabilization rate would have the greatest impact on coagulant efficacy.

After clay and water are added, the rapid-mix chamber then ejects coagulant into the system, beginning the process of ‘precipitate enmeshment,’ also known as flocculation. The rapid mixing stage can be considered one of the most vital components of the coagulation-flocculation processes. At this stage, primary flocs tend to form and destabilization reactions occur. (Jiang, 2015). The smaller particles are physically enmeshed by the metal precipitates previously introduced. This generally occurs when the precipitates are beginning to form and settle (Bratby, 2006).

Parameters, such as pH, temperature, alkalinity, composition of precipitates and mixing speeds can impact how effective the coagulation process is. It has been researched that alum coagulant performs at its maximum capacity when immersed within a solution of pH levels between 6 and 7. Coagulant, when introduced to high alkalinity water, may need to be used in large amounts to stabilize pH at an optimal level. This is important because if an insufficient amount of coagulant is administered, many problems can occur, such as the pipe corrosion, pH destabilization and the formation of residues that can clog pipes. Another parameter that can dictate the quality of the coagulation-flocculation process is temperature. Lower temperature waters tend to “decrease the hydrolysis and precipitation kinetics” (Hart).

It has been determined through flow and tracer transport methods that vorticity field is the key parameter to use to discern areas of jet flow and recirculation zones within the contact chamber. The vorticity gradient and the flexion product shed the most mathematical insights on the topic of differentiating recirculation and jet zones, as well as fluid to fluid flow separations. From this, the team will have a mathematical analysis of the validity behind the qualitative results. The ratio of t90/t10, or the Morrill index, describes the travel time of 10% and 90% of the cumulative normalized tracer concentration observed at the outlet of the contact chamber.

The basis with which the indices were characterized was classified as a "black box" analysis since the mechanisms of mixing within the contact chamber were overlooked or not analyzed (Demirel and Aral, 2016). The objective of this experimental analysis of behavior of the conservative tracer in the contact chamber is to note the mixing of the chemical within recirculation zones where the tracer is briefly retained before release, as well as the interactions between the jet zones and recirculation zones. Identifying these interactions were important because they both played a role in the aggregate mixing process. The difficulties posed in this analysis were the monitoring methods utilized in literature. The index bases were derived by measurements made only at specific outlet points throughout the system. There was no data highlighting the mechanics of mixing within the contact chamber itself.

## Methods
### Experimental Design

The experiment setup was identical to the other Particle Removal subteams, High G Flocculation and High Rate Sedimentation, to standardize results.

![Schematic](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/Schematic.jpg?raw=true)

Figure: The experiment setup includes a contact chamber, a coiled flocculator, and a sedimentation tube.


![Complete_setup](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/Complete_setup.jpg?raw=true)

Figure: In the experimental setup, the water and clay mixture flows through the influent turbidimeter to the contact chamber. Coagulant is injected immediately before the contact chamber. The 1 rpm pump was added to control upflow velocity in the sedimentation tube.

The experiment setup models the flow of water through a plant on a lab scale (Figure):

1. The clay stock is prepared and mixed.
2. The flow of coagulant, water, and clay are controlled by the pumps.
3. The influent turbidimeter measures the turbidity of the clay-water mixture before entering the contact chamber and flocculator.
4. Coagulant is injected immediately before the contact chamber and mixes with the clay-water mixture in the contact chamber.
5. The coiled flocculator causes further collisions between clay particles and coagulant.
6. The sedimentation tube allows flocs to settle out of the water. The 1 rpm waste pump drains the excess flocs from the sedimentation tube.
7. The effluent turbidimeter measures the turbidity of the water exiting the plant.


The influent turbidity was controlled using a Proportional-Integral-Derivative (PID) controller on ProCoDA. The PID controller uses a feedback response loop to maintain the influent turbidity. The target influent turbidity was set to 10 NTU, and the values of P, i, and D were set to 0.5, 0.25, and 0, respectively.

![PIDcontrol](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/PIDcontrol.png?raw=true)

Figure: Schematic of experimental setup. The PID controller adjusts the clay pump speed to maintain an influent turbidity of 10 NTU. The water pump and coagulant pump were kept constant at 76 rpm and 20 rpm, respectively.

### Materials

1. Pumps
    - Easy-load Masterflex 1 RPM Pump (Floc Weir Discharge)
    - (2) Masterflex 1.6-600 RPM Pumps
      - Coagulant Pump
      - Clay Pump
    - (1) Masterflex 10-600 RPM Pump (Water Pump)
2. Turbidimeters
    - (2) HF Scientific Inc MicroTOL Turbidimeters 0-1000 NTU
      - Influent turbidimeter: measures influent stream after introduction of clay into raw water stream before entering contact chamber
      - Effluent turbidimeter: measures effluent stream after flow through sedimentation tube
3. Contact chamber
    - Clear polycarbonate pipe
      - 10 in (25.4 cm) length, 1 in (2.54 in) diameter
    - PVC pipe end caps
4. Tubing and Fittings
    - Hard Tubing
    - Microbore Tubing
    - Yellow-blue size soft tubing
    - Size 16 soft tubing
5. Stock solution containers
    - 5 L tank for clay stock
    - 5 L tank for coagulant stock
5. Materials for stock solutions
    - Raw water line
    - Distilled water (used for coagulant stock)
    - Kaolinite clay
    - Polyaluminum chloride (PACl) coagulant (70.9 g/L)

### Experimental Apparatus
The contact chamber was constructed with a length that is 10 times the diameter to model the dimensions of the turbulent jet stream ([Tsang et al. 2017](contact_chamber/contact-chamber-fall.pdf)). The turbulent jet creates eddies that recirculate near the pipe walls. By minimizing contact with the walls of the contact chamber, the amount of coagulant that adheres to the walls instead of the clay particles can be minimized.

![Contact_chamber](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/contact_chamber.png?raw=true)

Figure: The redesigned contact chamber, with a length that is ten times the diameter, to model the dimensions of the turbulent jet.



### Procedure
To maintain an upflow velocity in the sedimentation tube of 2 mm/s, the water pump was kept constant at 76 rpm, while the flow rate contributions of the clay and coagulant were determined to be negligible, due to the low flow rate through the microbore tubing. PID control was used to vary the speed of the clay pump to reach the target influent turbidity of 10 NTU. The clay stock solution was diluted, so that the clay pump speed could be reduced to minimize the flow rate contribution of the clay pump. The concentration of the clay stock was 0.4 g/L. The coagulant dose was set by manual input to 20 RPM. The coagulant stock and pump speed were fine-tuned to achieve an effluent turbidity of approximately 2 NTU. The concentration of coagulant stock is currently 0.1418 g/L. Both the coagulant stock concentration and pump speed are subject to change as the system is altered.

Before running an experiment, all valves were opened (raw water, floc weir outlet, and the waste stream outlet). The PID set point was adjusted from the OFF state to ON state, initiating the clay pump to feed the clay stock solution into the system. The water pump and coagulant pump were switched on and set to pre-determined pump speeds. The influent turbidity was allowed to reach its target turbidity of 10 NTU, and changes in the effluent turbidity were observed.

## Results and Analysis

Prior to running experiments, a red dye test was conducted to observe the fluid dynamics of the coagulant dose in the contact chamber. Red dye was added to the coagulant stock, which tracked the motion of coagulant in the contact chamber.
It was observed that there was more recirculation in the contact chamber than expected, which may have caused a significant portion of the coagulant to adhere to the walls of the contact chamber, rather than interact with the clay particles in the water. It is hypothesized that the slow flow rate of the coagulant injection into the contact chamber did not allow the coagulant to mix well, which may have contributed to the poor performance of the contact chamber in previous experiments.

To reduce the high recirculation in the contact chamber, the team decided to change the orientation of the contact chamber. The contact chamber was previously oriented in the upflow direction, with the coagulant injection and clay mixture flowing into the contact chamber from the bottom. The contact chamber was inverted, and a red dye test was conducted with the coagulant and clay mixture entering the contact chamber from the top.

![5hoursexperiment](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/Experiment%20Result%20after%205%20hours.png?raw=true)
Figure: The influent and effluent turbidimeter after an experiment runtime of 5 hours.

The experiment was run for 5 hours to observe the formation of the floc blanket in the sedimentation tube. The results differed significantly from the results of previous experiments run in Fall 2017. All parameters were held consistent to the parameters used in the Fall 2017 experiments, except for the longer experiment runtime. It was observed that the effluent turbidity did not decrease sufficiently. Some possible sources of errors were identified, and possible solutions were attempted. The first noticeable issue was the growth of algae on the sides of the sedimentation tube, which may have had an impact on the effluent turbidity. To solve this problem, the sedimentation tube was cleaned with pipe brushes and bleach. Another possible source of error is the lack of a floc blanket in the sedimentation tube. In the Fall 2017 experiments, the sedimentation tube was not cleaned out in between experiments, which allowed a floc blanket to form after repeated trials. In order to standardize results, the sedimentation tube was drained in between each experiment. However, since the influent turbidity very low, at 10 NTU, it was time-consuming to form a new floc blanket for each experiment. Therefore, the sedimentation tank was redesigned with smaller dimensions to allow the floc blanket to form in a shorter time period. Shortening the time taken to form the floc blanket increased the efficiency of experiments.


## Conclusions

From the series of tests to see the efficiency of contact chamber and the sedimentation tank in the system, it is concluded that the change in design might be required in both units. So, the next steps for the team will be conduct more research on fluid dynamics including the particles as well as identify the relationship between the residence time and particle removal.

## Future Work
Over the next several weeks, the sedimentation tube will be redesigned with smaller dimensions.
With the newly designed sedimentation tube and contact chamber, it is expected that results will be more consistent. It is hypothesized that ensuring the formation of the floc blanket during each experiment will improve results, thereby reducing the effluent turbidity. Another future task is measuring the headloss across the flocculator to quantify the impact of coagulant adhering to the walls of the flocculator. The contact chamber theoretically increases the probability of collisions between the clay particles and coagulant before the mixture enters the flocculation system. As a result, it is predicted that the contact chamber will allow the clay particles more time to interact with the coagulant, which will decrease the amount of free coagulant that adheres to the walls of the flocculator, and therefore decrease headloss across the flocculator.

## Bibliography
Logan, B. E., Hermanowicz, S. W., & Parker,A. S. (1987). A Fundamental Model for Trickling Filter Process Design. Journal (Water Pollution Control Federation), 59(12), 1029–1042.

<!-- # Manual -->
<!-- The goal of this section is to provide all of the guidance that would be necessary for a future team to pick up your work where you left off. Please try to be thorough and put yourselves in the shoes of a newcomer to the project. Below are some recommended sections, but the manual will likely take a slightly different form for each team. -->

## Fabrication Details
<!-- Include any information related to the fabrication of equipment, experimental apparatuses, or technologies. Include the purpose of each step and the fabrication methods used. Reference appropriate safety precautions. -->
The contact chamber was fabricated using a 25.4 cm (10 in) clear polycarbonate pipe. PVC caps were attached on the ends of the pipe using PVC cement to waterproof the contact chamber. Threaded push-to-connect connections were attached to each end of the contact chamber to allow tubing to be attached.

<!-- ## Special Components -->
<!-- If your subteam uses a particular part that is unique and you could foresee a future subteam needing to order it or learn more about it, please include basic information like the vendor where it was purchased, catalog/item number, and a link to any documentation. -->

## Experimental Methods
### Set-up

1. Open valves to raw water and waste streams.
2. Power on all three pumps: Coagulant, Clay, and Water.
3. Run clay solution mixer.
4. Set raw water and clay pump speeds manually.

### Experiment
1. Begin ProCoDA program.
2. Run until a steady-state floc blanket is achieved.
3. Track changes in the effluent turbidity.

### Cleaning Procedure
1. Run Water through the system until the floc blanket escapes the system.Turn off clay pump using ProCoDA.
2. Turn off all three pumps: Coagulant, Clay, and Water.
3. Close valves to raw water and waste streams.

<!-- ## Experimental Checklist -->
<!-- Another potential section could include a list of things that you need to check before running an experiment. -->

## ProCoDA Method File


### States
* OFF
  - Default state for the experimental apparatus while not recording experimental results. Controls the PID controlled clay pump for the plant.
* PID Control
  - State that powers the clay peristaltic pump into the plant. This flow rate is adjusted autonomously by the PID program responding to the variations in the influent turbidimeter. The raw water, coagulant stock, and waste pumps are all adjusted by manually based on previous calculations.

### Set Points
<!-- Here, you should list the set points used in your method file and explain their use as well as how each was calculated. -->
| Set Point                | Operation Type | Value |
|:------------------------ |:--------------:|:-----:|
| OFF                      |       1        |   0   |
| ON                       |       1        |   1   |
| Turb Target inf          |    Constant    |  10   |
| P                        |    Constant    | 500m  |
| i                        |    Constant    | 250m  |
| D                        |    Constant    |   0   |
| Influent Turbidimeter ID |    Constant    |   2   |
| Influent Turbidity       |    Variable    |  10   |
| Effluent Turbidimeter ID |    Constant    |   1   |
| Effluent Turbidity       |    Variable    |   2   |
| Pump Control (Clay)      |    Variable    |  N/A  |


## Python Code
<!-- $g$: gravity
$\sigma$: dispersion
$a$: amplitude
$h$: water depth
$H$: distance from wave crest to trough (2$a$)
$T$: wave period
$\lambda$: wavelength
$k$: wavenumber
$c_p$: celerity (wave phase speed)
$P$: pressure
$F$: force
$u$, $w$: x-velocity, z-velocity components -->

###Coagulant and Clay Stock Concentration Calculations
Calculates the concentration of clay and coagulant in the plant
given the stock concentrations.  

####Coagulant Stock Concentration
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
####Calculate coagulant stock concentrations
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
####Clay stock concentration
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
###Calculation of Residence Time
```python
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



```python
To convert the document from markdown to pdf
pandoc ContactChamber_Spring2018.md -o contact_chamber_Research_Report.pdf
```
