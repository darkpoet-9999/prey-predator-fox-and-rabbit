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
| `rabbit-step-cost`       | The energy cost of a rabbit for each single forward movement.       | 1               |
| `rabbit-gain-from-food`  | The energy gained by a rabbit from eating grass.                    | 5               |
| `rabbit-reprod-prob`     | The probability of a rabbit to reproduce per tick.                  | 6.00%           |
| `initial-number-foxes`   | The initial population of foxes.                                    | 100             |
| `initial-fox-energy`     | The initial energy of the foxes.                                    | 30              |
| `fox-sight-distance`     | The distance that the foxes can see.                                | 2               |
| `fox-hear-distance`      | The distance that the foxes can hear.                               | 2               |
| `fox-normal-speed`       | The forward movement of a fox per tick when searching for a rabbit. | 1               |
| `fox-run-speed`          | The forward movement of a fox per tick when chasing a rabbit.       | 5               |
| `fox-step-cost`          | The energy cost of a fox for each single forward movement.          | 1               |
| `fox-gain-from-food`     | The energy gained by a fox from eating a rabbit.                    | 10              |
| `fox-reprod-prob`        | The probability of a fox to reproduce per tick.                     | 1.00%           |
| `grass-count`            | The number of grass units in the environment.                       | 1500            |
| `hole-count`             | The number of hiding holes for rabbits.                             | 300             |
| `grass-regrowth-time`    | The grass regrowth time.                                            | 15              |


### Behavior Overview

In this agent-based model (ABM) implementation, foxes and rabbits have the ability to see and hear their surroundings. Rabbits search for grass within their sight range (`rabbit-sight-distance`) and move towards it. If no grass is visible, they move forward in a random direction, at an angle between -44 to +44 degrees, to locate food. Rabbits can also detect sounds within their hearing range (`rabbit-hear-distance`). If they detect a fox through sight or hearing, they flee at a higher speed (`rabbit-run-speed`) until they find an unoccupied hiding hole where they can stay safely for up to 5 ticks and potentially reproduce.

Similarly, foxes can locate rabbits using their sight (`fox-sight-distance`) and hearing (`fox-hear-distance`). If no rabbits are detected, foxes move at their normal speed (`fox-normal-speed`) in a random direction, within an angle of -44 to +44 degrees. Once a rabbit is detected, the fox pursues it at an increased speed (`fox-run-speed`). If the rabbit successfully escapes into a hiding hole, the fox continues searching for another rabbit.

During each time step, both foxes and rabbits have the potential to reproduce, based on the reproduction probabilities (`fox-reprod-prob` and `rabbit-reprod-prob`) set by the respective sliders.
