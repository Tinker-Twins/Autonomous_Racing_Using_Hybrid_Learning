# Autonomous Racing using a Hybrid Imitation-Reinforcement Learning Architecture

In this work, we present a rigorous end-to-end control strategy for autonomous vehicles aimed at minimizing lap times in a time attack racing event.

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

| ![Behavioral Cloning Loss](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2a.png) | ![GAIL Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2b.png) | ![Curiosity Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2c.png) |
|:------------------:|:-------------------:|:-------------------:|
| ![Extrinsic Reward](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2d.png) | ![Policy Entropy](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2e.png) | ![Episode Length](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_2f.png) |

## Deployment Results

Deployment results were reported as a direct comparison of 10 autonomous laps (represented in red color) against 100 manual laps by 10 different human players (represented in blue color).

![Human Players vs Autonomous Agent](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_3.png)

The autonomous agent not only exhibited superior performance by gaining 0.96 seconds over the best manual lap, but it also dominated the human players by 1.46 seconds with regard to the mean lap time. This dominance could be justified in terms of better trajectory optimization and lower reaction time of the autonomous agent.

| Best Manual Lap | Best Autonomous Lap |
| :--------------:| :-----------------: |
| ![Best Manual Lap Trajectory](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_4a.png) | ![Best Autonomous Lap Trajectory](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_4b.png) |
| ![Best Manual Lap Controls](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_5a.png) | ![Best Autonomous Lap Controls](https://github.com/Tinker-Twins/Autonomous_Racing_Using_Hybrid_Learning/blob/main/Media/Figure_5b.png) |

## Demo
Implementation demonstrations are available on [YouTube](https://www.youtube.com/playlist?list=PLY45pkzWzH98HT0U8xq2j9OjybFDIaFN0).

## Citation

We encourage you to cite the [following paper](https://arxiv.org/abs/2110.05437) if you use any part of this project for your research:

```bibtex
@eprint{AutoRACE-2021,
    doi = {10.48550/ARXIV.2110.05437},
    url = {https://arxiv.org/abs/2110.05437},
    author = {Samak, Chinmay Vilas and Samak, Tanmay Vilas and Kandhasamy, Sivanathan},
    keywords = {Robotics (cs.RO), Artificial Intelligence (cs.AI), Machine Learning (cs.LG), Neural and Evolutionary Computing (cs.NE), FOS: Computer and information sciences, FOS: Computer and information sciences},
    title = {Autonomous Racing using a Hybrid Imitation-Reinforcement Learning Architecture},
    publisher = {arXiv},
    year = {2021},
    copyright = {arXiv.org perpetual, non-exclusive license}
}
```
