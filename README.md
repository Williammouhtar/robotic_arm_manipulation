## MAIN GOAL AND USEFUL FUNCTIONS LEARNED:  
The goal of this project was getting a first introduction to the PyBullet library and getting started with robotic arm simulations

the robotic arm used here is the Franka Emika Panda, a 7-degree-of-freedom robotic arm with a two-finger gripper. The goal was to drop a cube in a 3d space close to the arm and make it reach it and grab it.

the following documentation was used to first get familiarized with useful functions:
https://github.com/bulletphysics/bullet3/blob/master/docs/Bullet_User_Manual.pdf

Namely: 
getJointInfo() to connect the index of each joint to its 3d representation,
resetJointState() to go back to the initial position of the arm,
set_gravity() to be able to set the gravity at the z axis to -9.81,
getJointState() to get the current joint state,
setJointMotorControlArray() that helps us choose the joints needed to move as well as different factors such as the force and the target position,
calculateInverseKinematics() arguably the most important function, calculates the kinematics (rotation angles needed from each joint) that allows the end effector of the robot to reach the position of the block


## ISSUES ALONG THE WAY:

1 - at first, not knowing that calculateInverseKinematics() exists, I thought I needed to go back to my relavend coursework (namely basics of robotics for manipulation) and calculate the rotation angles needed to get to the object.
2 - Didn't know that a sleeptime option was needed and the robot would move almost instantly, not allowing to see precisely what movement was happening along the way, only showing the end position. This issue was eventually solved using ChatGPT.

## HELP FROM LLM's:

for most of the functions used above, I was initially lost as to what the inputs / arguments must be as the documentation wasn't necessarily clear on that. This is where using a LLM such as ChatGPT helped greatly to explain the intuition behind them, what arguments need to be passed ,
and how they work by giving me sample codes / small illustrative examples to know what to do.
Of course, I also used it to fix syntax errors.
