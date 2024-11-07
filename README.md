# Hydraulic_systems_maintainance Using machine learning Techniques

## Table of Contents
- [Project description](#ProjectDescription)
- [Usage](#usage)
- [Documentation](#Documentation)
- [Conclusion](#Conclusion)




#### Project Description

Condition Monitoring of Hydraulic System Using Machine Learning.


- Hydraulic systems are vital for powering heavy machinery in industries such as construction, manufacturing, and aviation.
- Efficiency and Power: Known for their ability to transfer significant amounts of power efficiently with precise control over movement.
- Applications: Used in heavy-duty equipment like cranes, excavators, aircraft control systems, and hydraulic presses.
- Vulnerability to Wear and Tear: Despite their reliability, hydraulic systems are susceptible to component wear, fluid contamination, and pressure imbalances, 
  which lead to performance degradation and eventual failure.


What is Condition Monitoring?

Tracks the health of hydraulic systems using real-  time sensor data.
Critical in preventing unexpected failures and ensuring smooth operation.


Conventional condition monitoring models are limited by their inability to generalize across                                                                        varying hydraulic systems and load conditions.

Current models overfit specific datasets and struggle to adapt to new conditions.

Sharing data across companies for better models is restricted due to privacy and proprietary information.

Many models require extensive amounts of data for training, limiting their applicability in scenarios with scarce or private datasets


## Our Approach 
1. Transfer Learning (TL) 
2. Federated Learning (FL) 


Sensors data: 
   1. Pressure sensors (PS1-6): 100 Hz, 6000 attributes per sensor (6 sensors)
   2. Motor power sensor (EPS1): 100 Hz, 6000 attributes per sensor (1 sensor)
   3. Volume flow sensors (FS1/2): 10 Hz, 600 attributes per sensor (2 sensors)
   4. Temperature sensors (TS1-4): 1 Hz, 60 attributes per sensor (4 sensors)
   5. Vibration sensor (VS1): 1 Hz, 60 attributes per sensor (1 sensor)
   6. Efficiency factor (SE): 1 Hz, 60 attributes per sensor (1 sensor)
   7. Virtual cooling efficiency sensor (CE): 1 Hz, 60 attributes per sensor (1 sensor)
   8. Virtual cooling power sensor (CP): 1 Hz, 60 attributes per sensor (1 sensor)

Components in hydraulic system  as Targets for condition monitoring: 
   1. Cooler condition 
   2. Valve condition
   3. Internal pump leakage
   4. Hydraulic accumulator 
   5. stable flag


### Transfer learning is a machine learning technique where knowledge gained from one task is applied to improve the performance of another related task. 
![image](https://github.com/user-attachments/assets/df7b424e-6406-499b-bd4e-10960e5eb9b5)

## MODEL ARCHITECTURE
<img src="https://github.com/user-attachments/assets/9b7c36fc-c8d0-474a-b06b-34cf74274899" alt="Alt Text" width="500" height="500">

Epochs vs Accuracy graph (a) for Pump leakage and (b) for Valve condition.
![image](https://github.com/user-attachments/assets/0fc638c7-5917-4865-9d6d-80020d0ec5ea)

Epochs vs loss (a) for Pump leakage and (b) for Valve Switching condition.
![image](https://github.com/user-attachments/assets/955832a7-a693-4336-9e85-2a2466f15f84)

Confusion matrix (a) for pump leakage condition and (b) for valve switching condition
![image](https://github.com/user-attachments/assets/80849039-b7c2-4294-853f-4d5277dc8c91)

![image](https://github.com/user-attachments/assets/7dae44e0-81cc-4dd2-b161-b4600bcc7b22)




#### Usage
By using model3 and model31 as pre-trained model we can make the tranfer learning multitsk model. these models were created by codes given in pretrainedmodel31h5.ipynb
pretrainedmodel3h5.ipynb these files.

the Final model was created in file tranfer_learning_multitask_mlp.ipynb


#### Documentation
(#links)



#### Conclusion

- This study shows that multi-task transfer learning enhances predictive maintenance in hydraulic systems by sharing knowledge between related tasks like pump 
  leakage and valve condition monitoring.
- The multi-task model achieved accuracies of 94.33% for pump leakage and 93.65% for valve condition, demonstrating faster training convergence than traditional 
  task-specific models. 
- Transfer learning allowed knowledge gained from one dataset to enhance performance in related models.
- Federated learning is a viable solution for condition monitoring in hydraulic systems without compromising privacy.
- The approach ensures data privacy and reduces the need for extensive data sharing.
- Successful implementation of CNN for multi-output classification of hydraulic system components.






