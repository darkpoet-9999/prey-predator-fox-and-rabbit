# Async Learning Task: Prey-Predator Ecosystems

## Fox and Rabbit Simulation

### Model Details:
  In this asynchronous exercise, we modeled the predator and prey paradigm in complex systems based on the fox-rabbit-grass food chain. In this model, there are three agents: foxes, rabbits, and grass patches. The fox is the predator, the rabbit is the prey and grass is the food source of the rabbit. The Netlogo model has several sliders which can be used to observe various scenarios, as listed below:


### Slider Settings

| Slider Setting           | Description                                                         | Default Setting |
| ------------------------ | ------------------------------------------------------------------- | --------------- |
| `initial-number-rabbits` | The initial population of rabbits.                                  | 50              |
| `initial-rabbit-energy`  | The initial energy of the rabbits.                                  | 30              |
| `rabbit-sight-distance`  | The distance that the rabbit can see.                               | 1               |
| `rabbit-hear-distance`   | The distance that the rabbit can hear.                              | 2               |
| `rabbit-normal-speed`    | The forward movement of a rabbit per tick when searching for food.  | 1               |
| `rabbit-run-speed`       | The forward movement of a rabbit per tick when running from a fox.  | 5               |
| `rabbit-step-cost`       | The basal energy cost of a fox per tick.                            | 1               |
| `rabbit-gain-from-food`  | The energy gained by a rabbit from eating grass.                    | 5               |
| `rabbit-reprod-prob`     | The probability of a rabbit to reproduce per tick.                  | 6.00%           |
| `initial-number-foxes`   | The initial population of foxes.                                    | 100             |
| `initial-fox-energy`     | The initial energy of the foxes.                                    | 30              |
| `fox-sight-distance`     | The distance that the foxes can see.                                | 2               |
| `fox-hear-distance`      | The distance that the foxes can hear.                               | 2               |
| `fox-normal-speed`       | The forward movement of a fox per tick when searching for a rabbit. | 1               |
| `fox-run-speed`          | The forward movement of a fox per tick when chasing a rabbit.       | 5               |
| `fox-step-cost`          | The basal energy cost of a fox per tick.                            | 1               |
| `fox-gain-from-food`     | The energy gained by a fox from eating a rabbit.                    | 10              |
| `fox-reprod-prob`        | The probability of a fox to reproduce per tick.                     | 1.00%           |
| `grass-count`            | The number of grass units in the environment.                       | 1500            |
| `hole-count`             | The number of hiding holes for rabbits.                             | 300             |
| `grass-regrowth-time`    | The grass regrowth time.                                            | 15              |


### Behavior Overview

In this Agent-based model (ABM) implementation, the foxes and rabbits have the ability to see and hear. The rabbits can look around them and find grass at a rabbit-sight-distance and move towards it, however, if no grass can be seen, then it will move forward at a random angle between -44 to +44 angle looking for grass. Rabbits can also hear at a rabbit-hear-distance. If they see or hear a fox, they flee at a rabbit-run-speed until they see/find an unoccupied hiding-hole where they can safely hide from foxes. Inside the hiding hole, they can also reproduce and can stay safely for 5 ticks. Similarly, the fox can see at a fox-sight-distance and hear at a fox-hear-distance to locate rabbits. If no rabbits are detected, they move forward at a fox-normal-speed at a random angle between -44 to +44. Once a rabbit is detected, it chases the rabbit at fox-run-speed. If a rabbit successfully escapes the fox by hiding in a hole, it moves to search for another rabbit. Lastly, in each time step, both foxes and rabbits are able to reproduce based on the percentage set on the fox-reproduce-prob and rabbit-reproduce-prob sliders, respectively.

