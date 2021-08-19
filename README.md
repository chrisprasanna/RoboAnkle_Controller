
# RoboAnkle_Controller
Extensive and reliable LabVIEW program for real-time control of a robotic ankle-foot prosthesis.

## Project Goal
There are a large number of gait asymmetries seen in individuals with lower limb loss when compared to able-bodied individuals. Since asymmetrical loading of the lower limbs can lead to serious long-term medical conditions such as osteoarthritis, efforts must be made toward designing prosthesis systems that provide proper ankle function.

The objective of this project was to design a controller that coordinates the action of a powered ankle-foot prosthesis (PAFP) in order to minimize asymmetries between the lower limbs. Additionally, the controller must adapt to and maintain symmetrical gait during load-carrying conditions.

## Challenges
Common challenges for PAFP controller designs include: (i) accounting for personalized altered body mechanics of the amputee, (ii) avoiding manual tuning of subject-specific control parameters, and (iii) designing a control law that automatically adapts to the user and environment. Additionally, many control approaches rely on finite states are not continuous or adaptive to variable conditions.

## Solution
The controller was designed to be adaptive through the use of time-invariant state estimations which anticipate important gait events and variability. Additionally, a data-driven iterative learning trajectory optimization was implemented to reduce ankle kinematic asymmetries between the prosthetic and intact limbs. Furthermore, subject parameter tuning is unnecessary and there is no need for able-bodied trajectory data.

## Features
- Continuous state estimation based on wearable sensors, coordinate transforms, adaptive parameters, and PCA analysis
- Real-time LabVIEW code for executing deterministic control laws, sensor fusion, signal processing, data logging, and HMI commands via a wireless network
- Novel hierarchical control law consisting of an iteratively learned impedance tracking formula (high-level), state estiation based on a single IMU sensor (mid-level), and first principles inverse drivetrain model for current tracking (low-level)
- Data logging capabilities

## Acknowledgements
- Thank you to [Anthony Anderson](https://github.com/ajanders) for introducing me to LabVIEW and helping me troubleshoot code. 
