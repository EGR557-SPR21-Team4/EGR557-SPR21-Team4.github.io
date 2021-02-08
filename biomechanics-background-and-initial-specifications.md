>[Home](index.md)
# Biomechanics Background and Initial Specifications

## 1  Candidate Organism

  Team four designed their bio-inspired mechanism based on the biomechanics of the American Cockroach, also known as the Periplaneta Americana, shown in Fig 1. Although the critter stands 12 millimeters tall, it can compress its body enough to fit through crevices as small as 3 millimeters. Their six long and barbed legs allow them to run on inclined surfaces with speeds up to 50 body lengths per second.
  
  <p align="center"> 
  <img width="479" alt="Screen Shot 2021-02-08 at 4 08 05 PM" src="https://user-images.githubusercontent.com/75342978/107292907-d6815100-6a27-11eb-9f01-aa00b2e212af.png">
  </p> 
  
  Our team was able to filter through multiple sources of information in order to gain more background knowledge on the American Cockroach. The team found a total of five supplemental research papers [1-5] and narrowed them down to the three most beneficial [1, 2, 3]. Through these papers, the team was able to acquire physical and quantitative specifications of the insect. These details will be further discussed in the section below.
  
  The first paper researches the ability of the American Cockroach (Periplaneta Americana) to crawl through confined spaces and traverse through crevices. Experiments were conducted to observe the following: exoskeleton compression, exoskeleton material properties, crevice traversal, confined space crawling by varying ceiling heights (12 mm - free running height, 9 mm - crouched height, 6 mm - body compression height, 4 mm - minimum ceiling height), varying surface friction and dynamic compressive cycle tests. It was found that the cockroach could move through crevices as small as 4 mm, within 300-800 ms by compressing parts of their body to 41-57%. Even with body compression and changes in posture the cockroaches could crawl through vertical confined spaces at velocities 60 cm/s. At the smallest crevice height of 4 mm, the running velocity and stride length decreased, whereas stride period remained constant through all crevices. Toughness of the exoskeleton enabled cockroaches to withstand compressive forces three hundred times body weight while traversing through crevices, and up to nine hundred times body weight without injury. Antennae were used for exploration and to search for escape openings. Crevice traversal was divided into five stages: exploration and crevice detection, head traversal with entry and body orientation, Pronotum traversal, thorax traversal and  abdomen traversal [1]. 
  
  The other research paper focused on the buckling ability of the legs of a variety of insects including that of the American Cockroach. It is noted that  thin, hollow tubes tend to be known for their sturdiness in relation to their volume and weight but also have a high chance of buckling with high loads. The buckling that can result from these loads include both local and ovalisation. Local buckling causes kinks in very precise locations whereas ovalization makes what was once a circular tube more ovular. This paper looks into the feasibility of using FEA to model buckling loads as well as how different insects may have evolved with legs that prevent permanently damaging buckling from occurring. From this paper, it does not seem that the American Cockroach achieves its ability to fit into tight spaces as a result of temporary leg buckling. When it comes to the circular tubes of the cockroach leg, there is a risk of buckling due to cantilever forces [2].
  
  The final research paper observed the different motions the Periplaneta Americana (American cockroach) used at different speeds and calculated results based on the data acquired. The mass recorded is 0.83g +/- 0.07g. The maximum stride length was recorded to be 6cm. It was observed that for different speeds, different pairs or sets of pairs of legs were used. Even with this variation, the ground reaction forces were constant over the entire speed range. For speeds from 0.44 - 1.0 m/s, tripod motion was observed, whereas, for speeds from 1.0 - 1.5 m/s (50 bl/s), quadrupedal or bipedal motion was observed. Using various apparatus, like a force plate, and software for data acquisition, a number of quantities were measured such as the ground reaction forces, speed, and stride (period, frequency, length). The velocity and displacement of the centre of mass, energy recovery, kinetic and gravitational potential energy were calculated. It was found that both kinetic energy and gravitational potential energy were nearly in phase. For speeds above 1.0 m/s, aerial phase was observed. Horizontal, vertical and lateral kinetic energy of the centre of mass were calculated from velocity changes of the centre of mass. Gravitational potential energy of the centre of mass was calculated from vertical displacement. To lift and accelerate the centre of mass, mechanical power generated was a curvilinear function. Increasing stride length showed high speeds but no appreciable increase in stride frequency [3].

## 2 Bio-Inspired Robots

## 3 Technical Parameters

The following information was gathered from the most significant cockroach references. The data is later used to calculate biomechanical parameters and robot specifications. 

_**Table 1:** American Cockroach Data_

|Parameter|Unit|Value Range|Reference|
|---|---|---|---|
|Mass|mg|0.76 +/- 0.16|[1]|
|Body Length|mm|31.9 +/- 2.75|[1]|
|Height|mm|9-12|[1]|
|Speed|m/s|0.44 - 1.5 m/s (50 bl/s)|[3]|
|velocity|Cm s^-1|58.05 +/- 2.3|[1]|
|Stride Length|mm|20 - 60|[3]|
|Leg radius|mm|0.410 +/- 0.05|[2]|
|Leg Thickness|mm|0.063 +/- 0.02|[2]|
|Minimum height traversed|mm|3 - 4|[1]|
|Dist. from foot to body midline|mm|11.89 +/- 0.96|[1]|
|Est max force per leg (based on proposed surface friction setup in [1])|mN|~38.0|[1]|
|Est max forward thrust (based on proposed surface friction setup in [1])|mN|227.9|[1]|
|Est body drag (based on proposed surface friction setup in [1])|mN|24.71-224.80|[1]|
|Mean Energy Recovery|%|6.7 +/- 0.88|[3]|
|Peak vertical ground reaction force|mN|~ 1.14 - 1.44|[3]|

## 4 Mechanical Equations

The team decided to make a few assumptions before calculating the values below. The normal force from the ground is undamped, thus, the force the cockroach pushes into the ground will be met by an equal opposing force. Additionally, gravity is a constant 9.81m/sec2. The team will use 40mm for slide length calculations and a 0.2 coefficient of friction will be used.

## 4.1 Horizontal Thrust Force

We will calculate the force in the forward x direction given [12]. This will be equal to the sum of forces in the x direction. In this case:  Fx = FThrust - FFriction - FDrag. Ft(given: 227.9mN) - Ff(µ*m*g) - Fd(given: 30mN) = 227.9mN-.2*.76*9.81-30nM = 182.99mN. As a result, the total force needed to thrust forward is 183mN. 

## 4.2 Peak Power

We will calculate the total amount of power required per mass density of cockroaches. In this case: Power = Force * Velocity; P = 182.99mN (above equations) * .5805m/s = 106.23mw. When we divide this by the mass density of the cockroach we are left with the power per mass density which equates to 139.77 mw/g.

## 4.3 Expected Energy

We will calculate the kinetic energy of a cockroach using basic kinetic formulas. The amount of energy that is required for a cockroach to move depends on the mass and average velocity of the cockroach. As a result, the kinetic energy will rage based on the minimum and maximum mass of a cockroach [1]. Minimum Kinetic Energy = 0.5*m*v^2 = 0.5*0.6*(58Cm s^-1)^2  = 6.75E-7 J. Maximum Kinetic Energy = 0.5*m*v^2 = 0.5*0.92(based on big cockroach [1])*(58Cm s^-1)^2  = 1.035E-6 J. As a result, the average kinetic energy used by a cockroach ranges anywhere from 6.75E-7 J to 1.035E-6 J.

## 5 Figures From Literature

  <p align="center"> 
  <img width="449" alt="Screen Shot 2021-02-08 at 4 01 46 PM" src="https://user-images.githubusercontent.com/75342978/107292368-f3695480-6a26-11eb-83f2-f206991f0282.png">
  </p> 
  

  <p align="center"> 
  <img width="519" alt="Screen Shot 2021-02-08 at 4 02 24 PM" src="https://user-images.githubusercontent.com/75342978/107292405-0a0fab80-6a27-11eb-83aa-67c273ee23f1.png">
  </p> 

  <p align="center"> 
  <img width="362" alt="Screen Shot 2021-02-08 at 4 03 25 PM" src="https://user-images.githubusercontent.com/75342978/107292496-2f041e80-6a27-11eb-990a-bbbf1ebc8ac4.png">
  </p> 
  
  <p align="center">
  <img width="512" alt="Screen Shot 2021-02-08 at 4 04 26 PM" src="https://user-images.githubusercontent.com/75342978/107292581-535ffb00-6a27-11eb-86d5-ea3c3673ed85.png">
  </p> 
  
  <p align="center">
  <img width="439" alt="Screen Shot 2021-02-08 at 4 04 44 PM" src="https://user-images.githubusercontent.com/75342978/107292606-5e1a9000-6a27-11eb-8922-cda33eff47bb.png">
  </p> 
  
  <p align="center">
  <img width="491" alt="Screen Shot 2021-02-08 at 4 05 28 PM" src="https://user-images.githubusercontent.com/75342978/107292680-78546e00-6a27-11eb-92ca-5bb93d9d8cb6.png">
  </p> 
  
  <p align="center">
  <img width="459" alt="Screen Shot 2021-02-08 at 4 06 06 PM" src="https://user-images.githubusercontent.com/75342978/107292744-8e622e80-6a27-11eb-8369-1daf2b864ca7.png">
  </p> 
  
  <p align="center">
  <img width="471" alt="Screen Shot 2021-02-08 at 4 06 37 PM" src="https://user-images.githubusercontent.com/75342978/107292776-a174fe80-6a27-11eb-9325-5c21228759ad.png">
  </p> 
  







## 6 Engineering Drawing

  <p align="center">
  <img width="519" alt="Screen Shot 2021-02-08 at 4 07 02 PM" src="https://user-images.githubusercontent.com/75342978/107292805-b05bb100-6a27-11eb-8443-3422ec2d612e.png">
  </p> 

As depicted in Fig 11, the mechanism uses a sarrus linkage, spring, and cable to alter the height of the robot cockroach. When the system is decompressed, the spring will push on the sarrus linkage. With the use of a small motor, the robot can alter its height based on the amount of cable it retracts around the spool. This will allow the robot to alter its body based on the given environment/terrain. The cockroach uses its long back legs to thrust itself forward. Our design uses a similar approach to replicate this bio-inspired motion. A motor will be used in the rear legs of the cockroach in order to alter the angle at which the robot thrusts. Once the angle is set, the solenoids attached to the motors will activate and thrust the robot cockroach forward. Based on the external terrain, the angle of the back legs will change. The middle and front legs of the cockroach will not be attached to an actuator, instead they will be used to stabilize the mechanism. In future iterations, the middle and front legs would be designed similarly to the CRAM robot [9]. This would allow the mechanism to crawl using its middle and front legs, and thrust using the rear set of legs. 


## 7 Discussion

## 7.1 Rationale for Organism

_Discuss / defend your rationale for the size animal you selected in terms of your ability to replicate key features remotely with limited material selection._

Our team decided to model our bio-inspired mechanism after an American Cockroach. The cockroach is known to fit in spaces as small as 3mm, which is regularly referenced to the height of two stacked pennies [9]. For this reason, our team has decided to scale the mechanism up. It would be extremely difficult to develop a mechanism 3mm thin with the class budget. The actuators on our mechanism would outweigh the actual weight of a cockroach [1]. As a result, we will need to scale the design's mass up in order to mimic the weight to power density ratio of a cockroach [1]. 

## 7.2 Motor and Power Selection

_Find a motor and battery that can supply the mechanical power needs obtained above. Consider that motor efficiencies may be as high as 95%, but if you can’t find it listed, assume you find a more affordable motor at 50-70% efficiency. Compare the mechanical watts/kg for the necessary motor and battery vs the animal’s mechanical power/mass above? Which one is more energy dense?_

For motor efficiency the equation is power output over power input multiplied by 100%. To get the power output of the mechanical system, the velocity of a biological cockroach was used, .5808 meters per second. This required changing into angular velocity  by multiplying by 2 PI. This yielded 3.6474mN. Taking the torque of a Faulhaber Series 2668 DC-micromotor, the specified motor which is 68nM and multiplying by the angular velocity, 248.02mw was obtained. Using the motor chart for power in of 254.3mw, the motor efficiency was calculated to be 97.53%. In order to obtain the power density, the power out (254.3mw) was divided by the size of the motor assembly (189g) which yielded a density of 1.31mw per gram. When compared to the power density ratio of a biological cockroach (formula seen in previous section) of 139.77mw/g there is no contest between the two; clearly, the cockroach has a higher energy density.






[References](references.md)

*[1]	K. Jayaram, "Robustness of Biological and Bio-Inspired Exoskeletons." Order No. 
10187254, University of California, Berkeley, Ann Arbor, 2015.

*[2] 	Eoin Parle, Simona Herbaj, Fiona Sheils, Hannah Larmon, David Taylor, “Buckling 
failures in insect exoskeleton”, Bioinspiration & biomimetics, 2015-12-17, Vol.11 (1).

*[3] 	Robert J. Full, Michael S. Tu, “Mechanics of a rapid running insect: Two-, Four- and 
Six-legged locomotion”, J. exp. Biol, 156,215-231, 1991.

 [4] 	Fred Delcomyn, “The locomotion of the cockroach Periplaneta Americana”, J. Exp. Biol, 
54. 443-452, 1971.

[5]	 D. L. DALEY, “The giant interneurons of the American Cockroach: Morphology and 
Physiology during walking.”, Order No. 7913419, University of Illinois at Urbana-Champaign, Ann Arbor, 1978.

*[6] 	D. L. Jindrich and R. J. Full, “Many-legged maneuverability: Dynamics of turning in 
hexapods,” J. Exp. Biol., vol. 202, no. 12, 1999.

*[7] 	A. M. Hoover, S. Burden, X. Y. Fu, S. S. Sastry, and R. S. Fearing, “Bio-inspired design 
and dynamic maneuverability of a minimally actuated six-legged robot,” 2010, doi: 10.1109/BIOROB.2010.5626034.

*[8] 	Y. C. Chou, W. S. Yu, K. J. Huang, and P. C. Lin, “Bio-inspired step-climbing in a 
hexapod robot,” Bioinspiration and Biomimetics, vol. 7, no. 3, 2012, doi: 10.1088/1748-3182/7/3/036008.

[9] 	K. Jayaram and R. J. Full, “Cockroaches traverse crevices, crawl rapidly in confined 
spaces, and inspire a soft, legged robot,” Proc. Natl. Acad. Sci. U. S. A., vol. 113, no. 8, 2016, doi: 10.1073/pnas.1514591113.

[10] 	A. M. Hoover, E. Steltz, and R. S. Fearing, “RoACH: An autonomous 2.4g crawling 
hexapod robot,” 2008, doi: 10.1109/IROS.2008.4651149.

[11]	“Tutorial on Embodiment,” Exploiting self-adaptation: cockroaches climbing over 
obstacles. [Online]. Available: https://www.eucognition.org/index.php?page=exploiting-self-adaptation-cockroaches-climbing-over-obstacles. [Accessed: 07-Feb-2021]. 

[12]	OpenStax, “University Physics Volume 1,” 5.7 Drawing Free-Body Diagrams | 
University Physics Volume 1, 03-Aug-2016. [Online]. Available: https://courses.lumenlearning.com/suny-osuniversityphysics/chapter/5-7-drawing-free-body-diagrams/. [Accessed: 08-Feb-2021].
