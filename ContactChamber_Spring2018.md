# Contact Chamber, Spring 2018
#### Cheer Tsang, Yeonjin Yun, Canaan Delgado
#### March 9, 2018

## Abstract
Briefly summarize your previous work, goals and objectives, what you have accomplished, and future work. (100 words max)

## Introduction
Explain how the completion of your challenge will affect AguaClara and the mission of providing safe drinking water (or sustainable wastewater treatment!). If this is a continuing team, how will your contribution build upon previous research? What needs to be further discovered or defined? If this is a new team, what prompted the inclusion of this team?

## Literature Review and Previous Work
Discuss what is already known about your research area based on both external work and that of past AguaClara Teams. Connect your objectives with what is already known and explain what additional contribution you intend to make. Make sure to add APA formatted in-text citations. If you mention the author(s) in your sentence, you can simply give the year of publication.[(Logan et. al. 1987)](http://www.jstor.org/stable/pdf/25043431.pdf?acceptTC=true)


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
The contact chamber was constructed with a length that is 10 times the diameter to model the dimensions of the turbulent jet stream. The turbulent jet creates eddies that recirculate near the pipe walls. By minimizing contact with the walls of the contact chamber, the amount of coagulant that adheres to the walls instead of the clay particles can be minimized.

![Contact_chamber](https://github.com/AguaClara/contact_chamber/blob/master/Diagrams/contact_chamber.png?raw=true)

* Design (calculations, constraints)

  $\frac{-b\pm\sqrt{b^2-4ac}}{2a}$
* Schematic (label parts)

  <img src="https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/IMG_0009.jpg?raw=true" height=250 width=200>

* Image (from lab; label parts)
* Materials (dimensions, materials)
* Complications in construction
* If already constructed: write a brief summary of important constraints, include any revisions to apparatus, also reference the prior report where construction is described

### Procedure
PID control is used to control the clay pump to reach the influent turbidity at 10. Clay stock solution was prepared to make sure the pump sped of the clay pump not to be too fast, if it was too fast, it will cause the change in upflow velocity constantly as the PID control will change the pump speed according to the influent turbidity.The concentration of the clay pump was determined to be 0.4g/L. The actual contribution of clay solution to upflow speed is almost negligible, since the microbore tubing was used. Water pump speed was set constant at 76 RPM to keep the upflow velocity at 2mm/s. The coagulant dose was set by a manual input to reach an effluent turbidity of approximately 2 NTU. The concentration of coagulant stock is 0.1418g/L. The pump speed now is 20 RPM with microbore tube, but both concentration and pump speed are subject to change as the system develops.

From the inputs determined, all valvues wre open (raw water, floc wir outlet, and the waste stream outlet). THe PID set point was adjusted from the OFF state to On state, initiating the clay pump to feed the clay stock solution into the system. Water pump and coagulant pump were powered. They clay pump speed adjusted itself responding to changes in the influent turbidimeter in order to maintain the turbidity at 10 NTU over the coure of the experimental trials.

## Results and Analysis





Present an observation (results), then explain what happened (analysis).  Each paragraph should focus on one aspect of your results. In that same paragraph, you should interpret that result.  
In other words, there should not be two distinct paragraphs, but instead one paragraph containing one result and the interpretation and analysis of this result. Here are some guiding questions for results and analysis:

When describing your results, present your data, using the guidelines below:
* What happened? What did you find?
* Show your experimental data in a professional way.
```python
from aide_design.play import*
x = np.array([1,2,3,4,5])
y = np.array([1,2,3,4,5])
plt.figure('ax',(10,8))
plt.plot(x,y,'*')
plt.savefig('/Users/jillianwhiting/github/Jillian-Whiting/Images/linear')
plt.show()
```
![linear](https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/linear.png?raw=true)
Figure 1: Captions are very important for figures. Captions go below figures.

After describing a particular result, within a paragraph, go on to connect your work to fundamental physics/chemistry/statics/fluid mechanics, or whatever field is appropriate. Analyze your results and compare with theoretical expectations; or, if you have not yet done the experiments, describe your expectations based on established knowledge. Include implications of your results. How will your results influence the design of AguaClara plants? If possible provide clear recommendations for design changes that should be adopted. Show your experimental data in a professional way using the following guidelines:
* Why did you get those results/data?
* Did these results line up with expectations?
* What went wrong?
* If the data do not support your hypothesis, is there another hypothesis that describes your new data?

## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

## Bibliography
Logan, B. E., Hermanowicz, S. W., & Parker,A. S. (1987). A Fundamental Model for Trickling Filter Process Design. Journal (Water Pollution Control Federation), 59(12), 1029–1042.

# Manual
The goal of this section is to provide all of the guidance that would be necessary for a future team to pick up your work where you left off. Please try to be thorough and put yourselves in the shoes of a newcomer to the project. Below are some recommended sections, but the manual will likely take a slightly different form for each team.

## Fabrication Details
Include any information related to the fabrication of equipment, experimental apparatuses, or technologies. Include the purpose of each step and the fabrication methods used. Reference appropriate safety precautions.

## Special Components
If your subteam uses a particular part that is unique and you could foresee a future subteam needing to order it or learn more about it, please include basic information like the vendor where it was purchased, catalog/item number, and a link to any documentation.

## Experimental Methods
### Set-up
Step 1.
* Put tasks in a sequential order.
* It is okay to have sub-lists.
  - Like this.

### Experiment
Step 1.

### Cleaning Procedure
Step 1.

## Experimental Checklist
Another potential section could include a list of things that you need to check before running an experiment.

## ProCoDA Method File
Use this section to explain your method file. This could be broken up into several components as shown below:

### States
Here, you should describe the function of each state in your method file, both in terms of its overall purpose and also in terms of the details that make it distinct from other states. For example:
\begin{itemize}
\item \underline{OFF} - Resting state of ProCoDA. All sensors, relays, and pumps are turned off.
\end{itemize}

### Set Points
Here, you should list the set points used in your method file and explain their use as well as how each was calculated.

## Python Code

### Variables
$g$: gravity
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
$u$, $w$: x-velocity, z-velocity components

```python
# Comment
```

```python
# To convert the document from markdown to pdf
pandoc ContactChamber_Spring2018.md -o contact_chamber_Research_Report.pdf
```
