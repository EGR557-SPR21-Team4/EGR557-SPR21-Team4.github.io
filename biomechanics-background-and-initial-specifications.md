>[Home](index.md)

# Biomechanics Background and Initial Specifications

## 1  Candidate Organism

  Team four designed their bio-inspired mechanism based on the biomechanics of the American Cockroach, also known as the Periplaneta Americana, shown in Fig 1. Although the critter stands 12 millimeters tall, it can compress its body enough to fit through crevices as small as 3 millimeters. Their six long and barbed legs allow them to run on inclined surfaces with speeds up to 50 body lengths per second.
  
  <p align="center"> 
  <img width="238" alt="Screen Shot 2021-03-28 at 10 45 57 PM" src="https://user-images.githubusercontent.com/75342978/112791951-5df64400-9017-11eb-8ef3-635806426484.png">
  </p> 
  
 Our team was able to filter through multiple sources of information in order to gain more background knowledge on the Razor Clam. The team found a total of five supplemental research papers [1-5] and narrowed them down to the three most beneficial [1, 2, 3]. Through these papers, the team was able to acquire physical and quantitative specifications of the clam. These details will be further discussed in the section below. 
  
  The first paper researches  [1]. 
  
  The second research paper focuses on[2].
  
  The final research paper observs [3].

## 2 Bio-Inspired Robots

After analyzing the research papers on the razor clam, five sources [6-10] were found that use the organism to create a biomechanical robot. After narrowing the results down to three papers [6, 8, 9],  the team studied and gathered the biomechanical data described in the section below.


 The first research paper is a nearly 300 page dissertation which includes a great amount of information pertaining to the razor clam and it’s burrowing mechanics and kinematics. There is an indepth look at the burrowing mechanism of bivalve clams, which is what we are modeling as our bioinspiration. This also contains more information about categorization of different clams than we could ever need. Furthermore, this research showcases 4 different bioinspiration based robots- worm, root, clam, and wasp based robots. There are mathematical analytical models for the kinematics which could help with kinematic calculations for this team. 
[6]. 
  
 The second research produced one of the only robotic solutions based on clams that is not ‘RoboClam’. This paper measures both burrowing and non borrowing speed and time required for a similar mechanism as the Razor Clam uses. Table 3 (page 15) has good information about soil and actuator properties pertaining to this research. Some of these values may be of use when working on the kinematics and solution of this team's robot. Figure 4 showcases an extremely useful diagram for understanding the burrowing mechanism for the razor clam which this paper directly translates into a robotic mechanism for movement. [7]. 
  
  The third report refers to a Conducted study that tests the validity of localized fluidization of burrowing as a delivery method for pipe installation. Focusing on the Ensis directus due to its high energy to depth of dig ratio allowed this study to create Roboclam 2- a more self contained actuator system than the first Roboclam. The design parameters and fluidization information is beneficial for the list of values and equations necessary for the realization of this project. Ultimately, the Roboclam 2 design would yield 255 N of downwards force while providing 1020 N of the shell expansion force. This will help answer how efficient current robotics are to the biological model [8]. 


## 3 Technical Parameters

The following information was gathered from the most significant Razor Clam references. The data is later used to calculate biomechanical parameters and robot specifications. 

<p align = "center"> <b> Table 1: </b> <i> Razor Clam Data </i></p>

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

The team decided to make a few assumptions before calculating the values below. The normal force from the ground is undamped, thus, the force the clam pushes into the ground will be met by an equal opposing force. Additionally, gravity is a constant 9.81m/sec2. The team will use 40mm for slide length calculations and a 0.2 coefficient of friction will be used.

## 4.1 Horizontal Thrust Force

We will calculate the force in the forward x direction given [12]. This will be equal to the sum of forces in the x direction. In this case:  Fx = FThrust - FFriction - FDrag. Ft(given: 227.9mN) - Ff(µ*m*g) - Fd(given: 30mN) = 227.9mN-.2*.76*9.81-30nM = 182.99mN. As a result, the total force needed to thrust forward is 183mN. 

## 4.2 Peak Power

We will calculate the total amount of power required per mass density of clams. In this case: Power = Force * Velocity; P = 182.99mN (above equations) * .5805m/s = 106.23mw. When we divide this by the mass density of the cockroach we are left with the power per mass density which equates to 139.77 mw/g.

## 4.3 Expected Energy

We will calculate the kinetic energy of a clam using basic kinetic formulas. The amount of energy that is required for a clam to move depends on the mass and average velocity of the clam. As a result, the kinetic energy will rage based on the minimum and maximum mass of a clam [1]. Minimum Kinetic Energy = 0.5*m*v^2 = 0.5*0.6*(58Cm s^-1)^2  = 6.75E-7 J. Maximum Kinetic Energy = 0.5*m*v^2 = 0.5*0.92(based on big cockroach [1])*(58Cm s^-1)^2  = 1.035E-6 J. As a result, the average kinetic energy used by a clam ranges anywhere from 6.75E-7 J to 1.035E-6 J.

## 5 Figures From Literature

  
  

  







## 6 Engineering Drawing

  <p align="center">
  <img width="519" alt="Screen Shot 2021-02-08 at 4 07 02 PM" src="https://user-images.githubusercontent.com/75342978/107292805-b05bb100-6a27-11eb-8443-3422ec2d612e.png">
  </p> 

As depicted in Fig X, the mechanism uses sarrus linkages, springs, and cables to alter the height of the robot clam. When the system is decompressed, the spring will push on the sarrus linkage. With the use of a small motor, the robot can alter its height based on the amount of cable it retracts around the spool. This will allow the robot to alter its body based on the given environment/terrain. The razor clam uses its “foot” to stretch out and burrow into the ground. From there, the end of the foot expands to create an “anchor”, which allows it to pull the rest of its body towards the anchor.


## 7 Discussion

## 7.1 Rationale for Organism

_Discuss / defend your rationale for the size animal you selected in terms of your ability to replicate key features remotely with limited material selection._

Our team decided to model our bio-inspired mechanism after an American Cockroach. The cockroach is known to fit in spaces as small as 3mm, which is regularly referenced to the height of two stacked pennies [9]. For this reason, our team has decided to scale the mechanism up. It would be extremely difficult to develop a mechanism 3mm thin with the class budget. The actuators on our mechanism would outweigh the actual weight of a cockroach [1]. As a result, we will need to scale the design's mass up in order to mimic the weight to power density ratio of a cockroach [1]. 

## 7.2 Motor and Power Selection

_Find a motor and battery that can supply the mechanical power needs obtained above. Consider that motor efficiencies may be as high as 95%, but if you can’t find it listed, assume you find a more affordable motor at 50-70% efficiency. Compare the mechanical watts/kg for the necessary motor and battery vs the animal’s mechanical power/mass above? Which one is more energy dense?_

For motor efficiency the equation is power output over power input multiplied by 100%. To get the power output of the mechanical system, the velocity of a biological cockroach was used, .5808 meters per second. This required changing into angular velocity  by multiplying by 2 PI. This yielded 3.6474mN. Taking the torque of a Faulhaber Series 2668 DC-micromotor, the specified motor which is 68nM and multiplying by the angular velocity, 248.02mw was obtained. Using the motor chart for power in of 254.3mw, the motor efficiency was calculated to be 97.53%. In order to obtain the power density, the power out (254.3mw) was divided by the size of the motor assembly (189g) which yielded a density of 1.31mw per gram. When compared to the power density ratio of a biological cockroach (formula seen in previous section) of 139.77mw/g there is no contest between the two; clearly, the cockroach has a higher energy density.






[References](references.md)

*[1]	

*[2] 	

*[3] 	
 [4] 	

[5]	 

*[6] S. Huang, "Self-Burrowing Mechanism and Robot Inspired by Razor Clams," ProQuest Dissertations Publishing, Tempe, 2020.	

*[7] 	https://www.google.com/url?q=https://iopscience-iop-org.ezproxy1.lib.asu.edu/article/10.1088/1748-3190/ab8754/pdf&sa=D&source=editors&ust=1616997857243000&usg=AOvVaw1G8c1kk5Hh0k4j8HWz8zAD

*[8] 	https://dspace.mit.edu/bitstream/handle/1721.1/98251/Dan%20IDETC%20Paper%20Final%20Post%20Reviews.pdf?sequence=1&isAllowed=y

[9] 	

[10] 	

[11]	

[12]	
