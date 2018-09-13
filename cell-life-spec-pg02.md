### What Cells See

Cells see in convolutions of 7x7 (or something odd, but 7x7 feels like enough complexity for it to be interesting but not too much data)

```
######### Example input. Each square would give some information
#   X   # 
# X     # [Color distance] <- if individual
#       # [Food amount] <- if square currently on
#   0   # [0] <- if nothing
#       # 
#       # Senses would be appended such that:
# X     # Most mates direction [0, 1, 2, 3] / [N, E, S, W]
######### Most food direction, etc
```

Each cell has to determine: [Nothing, Move up, move down, move left, move right, eat, fight, mate]

Cell attributes:
Age
Strength
Energy

Energy is the same as health.

Energy = 500
Age = 0

Every 10 steps, age += 1, max energy -= 1
