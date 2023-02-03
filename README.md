# Autonomous Racing using a Hybrid Imitation-Reinforcement Learning Architecture

In this work, we present a rigorous end-to-end control strategy for autonomous vehicles aimed at minimizing lap times in a time attack racing event. Deployment results were reported as a direct comparison of 10 autonomous laps against 100 manual laps by 10 different human players. The autonomous agent not only exhibited superior performance by gaining 0.96 seconds over the best manual lap, but it also dominated the human players by 1.46 seconds with regard to the mean lap time. This dominance could be justified in terms of better trajectory optimization and lower reaction time of the autonomous agent.

## Simulation System

The simulation system employed for validating the proposed pipeline was developed as a part of this research project, and was employed to simulate accurate vehicular and environmental dynamics along with realistic audio-visual effects. The source files of `AutoRACE Simulator` can be found [here](https://github.com/Tinker-Twins/AutoRACE-Simulator).

The simulator supports both manual and autonomous racing events, and offers the flexibility of designing various types of racing events. This work particularly focuses on [time attack racing](https://en.wikipedia.org/wiki/Time_trial).

![AutoRACE Simulator](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Human_vs_AI.png)

## Hybrid Imitation-Reinforcement Learning Architecture 

We adopted a hybrid imitation-reinforcement learning architecture and crafted a novel reward function to train a deep neural network policy to drive (using imitation learning) and race (using reinforcement learning) a car autonomously in less than 20 hours.

![AutoRACE Simulator](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_1.png)

## Training Results

The training phase of the proposed approach was analyzed in order to gain a better insight into the policy optimization process, and comment on the effectiveness of the hybrid learning strategy adopted in this work. Particularly, we analyzed the imitation learning (behavioral cloning loss, GAIL reward)
and reinforcement learning (curiosity reward, extrinsic reward) metrics along with the policy entropy and episode length.

|                    |                     |                     |
|:------------------:|:-------------------:|:-------------------:|
| ![Behavioral Cloning Loss](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2a.png) | ![GAIL Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2b.png) | ![Curiosity Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2c.png) |
| ![Extrinsic Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2d.png) | ![Policy Entropy](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2e.png) | ![Episode Length](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2f.png) |
|                    |                     |                     |
