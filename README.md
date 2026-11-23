# Sokoban Solver

[![make.fun](https://make.fun/badge/sokoban-solver-01-run-20261121.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121)
[![Rank](https://make.fun/badge/sokoban-solver-01-run-20261121/SkyScrapperR/sokoban-solver/rank.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121)
[![Reward](https://make.fun/badge/sokoban-solver-01-run-20261121/SkyScrapperR/sokoban-solver/reward.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121)

Push-optimal, room-decomposed Sokoban solver built for the make.fun bounty.

## Approach
- **Room Decomposition**: Detects the central hallway row and decomposes the board into independent room components. Since hallway cells are dead squares for boxes, boxes never leave their respective rooms, allowing each room to be solved independently to its exact push optimum.
- **Push-Optimal BFS**: Explores the state space over box configurations and normalized player reachable regions, pruned by reverse-pull dead-square analysis and 2x2 frozen deadlock detection.
- **Move Optimization**: Tests room permutations to minimize overall player walking moves between room doors across the hallway.

## License
MIT
