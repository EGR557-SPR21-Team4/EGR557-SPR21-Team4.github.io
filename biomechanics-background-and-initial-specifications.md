>[Home](index.md)

# Biomechanics Background and Initial Specifications

## 1  Candidate Organism

  Team four designed their bio-inspired mechanism based on the biomechanics of the Razor Clam, such as the Ensis Magnus, shown in Fig 1. Although this creature's small size limits its digging abilities to a few centimeters, it is very efficient given the mode of locomotion uses only its foot and shell.
  
  <p align="center"> 
  <img width="472" alt="Screen Shot 2021-04-05 at 10 20 43 PM" src="https://user-images.githubusercontent.com/75342978/113662558-2b72c980-965d-11eb-856e-5e1ffd8b6fbc.png">
  </p> 
  
 Our team was able to filter through multiple sources of information in order to gain more background knowledge on the Razor Clam. The team found a total of five supplemental research papers [1-5] and narrowed them down to the three most beneficial [1, 2, 3]. Through these papers, the team was able to acquire physical and quantitative specifications of the clam. These details will be further discussed in the section below.  
  
 The first paper, while focusing on razor clams in Wales, goes into detail regarding the Ensis family, describing the differences between them and other razor clam species as well as the differences in subspecies within the family. Ensis razor clams are differentiated from other types of razor clams by their “hinge teeth.” Ensis spp have two teeth on their left valve, which fits a tooth that is on the right valve. Ensis spp are also described as having delicate, smooth, long shells whose interior is white, while the exterior is a combination of vague red- and purple-brown markings with a thin green skin-like coating. Generally, Ensis species reside in areas where the sediment is at least 30 cm deep with relatively high levels of tidal movement. Specific Ensis species tend to have a unique set of tolerances of environments in which they can live, variables ranging from temperature to sediment grain size. This paper focuses on the three most common Ensis species most fished in Welsh waters. These species range from 125 - 200 mm in length and can be found from the shore to waters over 40 meters deep. It was found that they use their foot to bury themselves vertically over 1 meter into the ground. Some species have also been seen using their foot as a paddle and siphoning water out to move 3 - 5 meters per burst. The paper then goes on to discuss other topics that are not pertinent to the teams research, such as information regarding predictive distribution and some of the harvesting methods in place[1].
 
 The second paper focuses on the Atlantic Razor Clam (Ensis directus) as a means of reference for developing new burrowing technology. Many different types of burrowing and anchoring organisms were studied during this research, but bivalves such as the razor clams stood out as actively reducing the energy required for burrowing. The movement of the Ensis directus is initiated by the foot, which reaches down into the sediment, after which the valves move upward and compress, pushing the blood into the end of the foot, which causes it to expand, acting as an anchor to which it can pull the rest of the body down. The energy used during each step of the burrowing process of the Atlantic Razor Clam which averages at about 18 cm in length, was calculated and yielded a total of 0.21 J/cm for one set of burrowing motions. A comparison was made pointing out that 0.21 J/cm would allow for the clam to (theoretically) “travel over half a kilometer on the energy in a AA battery.” They can burrow at about 1cm/s, to depths of about up to 70cm. The paper then goes into some comparisons of Ensis directus to existing technologies, which show that the organism is ultimately more efficient when looking at the force given the mass of the system/organism [2]. 
  
  The third paper uses discrete element method modeling to study the penetration kinematics of the Atlantic razor clam (Ensis directus), specifically the effects of the shell expanding on the surrounding environment. Similar to other research on razor clams, this paper starts by describing the steps the clam uses to burrow into the ground, with a maximum tension force of 10N when dragging the body down towards the end of the foot. It is pointed out that in order to pull itself through the sediment, the organism needs to be able to fluidize the surrounding material. Using varying expansion ratios and rates, general forces were able to be calculated. While burrowing, the maximum pressure on the body recorded was about 10kPa, and with a shell expansion of about 0.85 centimeters. This is said to be “equivalent to a lateral resting force of approximate 76 N” [3].

## 2 Bio-Inspired Robots

After analyzing the research papers on the razor clam, five sources [6-10] were found that use the organism to create a biomechanical robot. After narrowing the results down to three papers [6, 8, 9],  the team studied and gathered the biomechanical data described in the section below.


 The first research paper, unlike many of the other papers found, focuses more on the Ensis directus burrowing-out strategies as opposed to strategies to burrow deeper to the ground. Their studies had been used to develop a “simple self-burrowing out robot” known as SBOR. It was found that the organism, when buried 50mm into the sediment is able to come to the surface in 1.6 - 7.5 seconds with stride lengths averaging at 30.4 mm (4.5 - 46.7 mm), which is much quicker than when the clam is digging downward, which takes 20 - 63 seconds to reach the same 50mm level, with averaging stride lengths of 5mm. The razor clams motion can be represented with an actuator that has one degree of freedom, which is the direction taken with SBOR, which extends and contracts based on pressure. It is controlled by an Arduino Mega 2560 and also makes use of a miniature diaphragm air pump, four channel MOSFET, pneumatic solenoid valves, and pressure sensors, some of which may be useful when the team is determining which parts would be suitable for the fabrication process. It was determined that for the SBOR system, the actuator has a modulus value of 810 kPa, which would be lower if there was no fiber reinforcement. The SBOR system successfully was able to reach a close approximation of the burrowing distance over time to that of the living organism. Equations for values such as actuator tensional force, actuator extension, and frictional force are included as well as the properties and dimensions of the SBOR actuator, which gives the team a rough idea as to how a man-made system of a razor will look/weigh [6].
 
 The second research paper delves into the realm  of pipe climbing robots using origami and modular techniques, which is a very similar direction this project is planning on taking. In this research, there are a few different considerations, one of which is whether the robot will be climbing on the inside or outside of the pipe. All designs in this paper regarding the movement mechanics, use a type of bellows that expand and contract to move the body in the desired direction. The robot the team in this paper designed had a mass of 208 grams and was able to climb pipes of approximately 148mm. In our design, we would want this to be smaller and more adjustable, as the goal is to create something that can navigate in a range of tight vertical spaces. While not used in the in-pipe climbing robot, the team in this paper present an origami leg design that rests in an open position naturally and is able to vary its gripping diameter, whereas the other two designs have static legs that surround a soft actuator tube that pokes through gaps in the hard leg to create the friction necessary to hold the robot in place. There are many equations provided and used within this paper, such as equations to calculate the strain-energy stored and the work of the air pressure. All equations are mentioned and used in context, and can be useful when calculating our own coefficients and values [7].  
  
  The third research paper focuses on the mechanics of burrowing by localized fluidization. Through experimental validation, it is shown that the Atlantic Razor Clam’s burrowing method is transferable to bio-inspired engineering implementation, such as through the design and implementation of RoboClam.The purpose of creating the RoboClam is to test a machine that burrows via localized fluidization, which is an effective method for reducing energy costs related to diggind RoboClam consists of a control platform that contains two pneumatic pistons. These pistons actuate the end-effector to follow the motion of the valves of the clam (up-in-down-out). The end-effector is enclosed in a rubber boot to prevent soil particles from jamming it. A sliding wedge moves the two valves in and out, to achieve displacement. To prevent jamming during the stroke, the wedge and valves are exactly constrained. The control system of the RoboClam integrates the forces acting on the pneumatic actuators over their displacement, in order to track the total amount of input energy to the system.  Genetic algorithm (GA) was used to find optimal digging kinematics, which controls RoboClam. The GA runs a test using a random set of instructions which includes displacements, pressure etc. and records the robot’s performance. The instructions are then optimized for digging efficiency by comparing them to a metric. The instructions that give a high cost are discarded and a new set of instructions are formed and run on the robot. This process is run multiple times. Finally a set of instructions are obtained that are optimized for efficient digging by the robot. In conclusion, the RoboClam was able to achieve localized fluidization by following the burrowing motion of the clam itself. The results found through this paper forms a base from which machines using localized fluidization for burrowing can be designed for different types of soil[8]. 


## 3 Technical Parameters

The following information was gathered from the most significant Razor Clam references. The data is later used to calculate biomechanical parameters and robot specifications. 

<p align = "center"> <b> Table 1: </b> <i> Razor Clam Data </i></p>

|Parameter|Unit|Value|Reference|
|---|---|---|---|
|Body Length|cm|18;  12.5-20|[2]  [1]|
|Shell Expansion|cm|0.85|[3]|
|Velocity Downward|cm/s|1|[2]|
|Stride Length Upward (in sediment)|mm|30.4;  4.5-46.7|[5]|
|Stride Length Downward|mm|5|[5]|
|Stride Length (Swimming E. magnus)|m|3-5|[1]|
|Energy of one Burrowing Cycle|J/cm|0.21|[2]|
|Peak Vertical Ground Reaction Force|N|10|[3]|
|Peak Pressure on Organism|kPa|10|[3]|
|Burrowing Depth|cm|70|[2]|


## 4 Mechanical Equations

The team decided to make a few assumptions before calculating the values below. The normal force from the ground is undamped, thus, the force the clam pushes into the ground will be met by an equal opposing force. Additionally, gravity is a constant 9.81m/sec2. The team will use 40mm for slide length calculations and a 0.2 coefficient of friction will be used.

## 4.1 Vertical Thrust Force

We will calculate the force in the forward x direction given [12]. This will be equal to the sum of forces in the x direction. In this case:  Fx = FThrust - FFriction - FDrag. Ft(given: 227.9mN) - Ff(µ*m*g) - Fd(given: 30mN) = 227.9mN-.2*.76*9.81-30nM = 182.99mN. As a result, the total force needed to thrust forward is 183mN. 

## 4.2 Peak Power

We will calculate the total amount of power required per mass density of clams. In this case: Power = Force * Velocity; P = 182.99mN (above equations) * .5805m/s = 106.23mw. When we divide this by the mass density of the cockroach we are left with the power per mass density which equates to 139.77 mw/g.![Uploading Screen Shot 2021-04-05 at 10.27.00 PM.png…]()


## 4.3 Expected Energy

We will calculate the kinetic energy of a clam using basic kinetic formulas. The amount of energy that is required for a clam to move depends on the mass and average velocity of the clam. As a result, the kinetic energy will rage based on the minimum and maximum mass of a clam [1]. Minimum Kinetic Energy = 0.5*m*v^2 = 0.5*0.6*(58Cm s^-1)^2  = 6.75E-7 J. Maximum Kinetic Energy = 0.5*m*v^2 = 0.5*0.92(based on big cockroach [1])*(58Cm s^-1)^2  = 1.035E-6 J. As a result, the average kinetic energy used by a clam ranges anywhere from 6.75E-7 J to 1.035E-6 J.

## 5 Figures From Literature

  
  
<p align="center"> 
  <img width="375" alt="Screen Shot 2021-04-05 at 10 27 49 PM" src="https://user-images.githubusercontent.com/75342978/113663051-295d3a80-965e-11eb-8dfa-6c4cb1c0cc95.png">  
</p> 

<p align="center"> 
 <img width="537" alt="Screen Shot 2021-04-05 at 10 31 59 PM" src="https://user-images.githubusercontent.com/75342978/113663359-bdc79d00-965e-11eb-957f-01befabcb977.png">
</p> 

<p align="center"> 
 <img width="484" alt="Screen Shot 2021-04-05 at 10 34 40 PM" src="https://user-images.githubusercontent.com/75342978/113663568-1dbe4380-965f-11eb-8a23-f2dd02cdf66d.png"> 
</p> 

<p align="center"> 
  
</p> 

<p align="center"> 
  
</p> 

<p align="center"> 
  
</p> 

<p align="center"> 
  
</p> 

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






## References

[1] Fraser, S., Shelmerdine, R.L., and Mouat, B, “Razor clam biology, ecology, stock assessment, and exploitation: a review of Ensis spp. in Wales,” in NAFC Marine Centre, 2018.

[2] A. G. Winter and A. E. Hosoi, “Identification and evaluation of the atlantic razor clam (Ensis directus) for biologically inspired subsea burrowing systems,” in Integrative and Comparative Biology, 2011, vol. 51, no. 1, doi: 10.1093/icb/icr038.

[3] S. Huang and J. Tao, “Modeling of the Burrowing Mechanism by Razor Clam: Role of Penetration Kinematics,” 2018, doi: 10.1061/9780784481585.053.

[4] S. Huang and J. Tao, “Modeling Clam-inspired Burrowing in Dry Sand using Cavity Expansion Theory and DEM,” Acta Geotech., vol. 15, no. 8, 2020, doi: 10.1007/s11440-020-00918-8.

[5] A. G. Winter, R. L. H. Deits, and A. E. Hosoi, “Localized fluidization burrowing mechanics of Ensis directus,” J. Exp. Biol., vol. 215, no. 12, 2012, doi: 10.1242/jeb.058172.

[6] J. J. Tao, S. Huang, and Y. Tang, “SBOR: a minimalistic soft self-burrowing-out robot inspired by razor clams,” Bioinspiration and Biomimetics, vol. 15, no. 5, 2020, doi: 10.1088/1748-3190/ab8754.

[7] Y. Jiang, D. Chen, H. Zhang, F. Giraud, and J. Paik, “Multimodal pipe-climbing robot with origami clutches and soft modular legs,” Bioinspiration and Biomimetics, vol. 15, no. 2, 2020, doi: 10.1088/1748-3190/ab5928.

[8] A. G. V Winter, R. L. H. Deits, D. S. Dorsch, A. H. Slocum, and A. E. Hosoi, “Razor clam to RoboClam: Burrowing drag reduction mechanisms and their robotic adaptation,” Bioinspiration and Biomimetics, vol. 9, no. 3, 2014, doi: 10.1088/1748-3182/9/3/036009.

[9] D. S. Dorsch and A. G. V. Winter, “Design of a low energy, self contained subsea burrowing robot based on localized fluidization exhibited by atlantic razor clams,” in Proceedings of the ASME Design Engineering Technical Conference, 2014, vol. 5A, doi: 10.1115/DETC2014-34953.

[10] K. N. Nordstrom, D. S. Dorsch, W. Losert, and A. G. Winter, “Microstructural view of burrowing with a bioinspired digging robot,” Phys. Rev. E - Stat. Nonlinear, Soft Matter Phys., vol. 92, no. 4, 2015, doi: 10.1103/PhysRevE.92.042204.
