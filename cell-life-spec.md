Interesting idea for a life simulation I thought of while working out.

A lot of life simulations use agents that rotate and move around a map with a neural network. I'm interested more in something like 'Gridworld' where agents get a picture of the environment around them and have to act in certain ways upon it.

The cells in this world will try to conquer as much land as possible and grow into their own species. Imagine a cellular automata on a Risk board.

Here are the rules of the world:

1. Cells have a color value which is similar to their species. They can only reproduce with species that are a certain color distance from them. This will create different colonies.

2. Cells have to eat. They can do this by eating plant food that is on the ground or killing other cells and eating their dead bodies (rip)

3. Plant food slowly grows back, but can be overeatten and then destroyed. Each tile on the map has a value of how much plant food is on it. Tiles with more plant food will replenish neighboring tiles faster than tiles will less plant food. This should incentivize cells to learn how to manage their resources.

4. Cells can kill other cells by attacking them. If a cell chooses to attack another cell, the battle will be decided based on the strength, health, and age of the two cells. The losing cell will die and leave it's meat on the ground which will slowly deplenish to simulate rotting.

5. If multiple cells choose to attack on their turn, their strengths will be added together. This will allow for 'team' play attacks.

6. Cells will have 'senses' of the world around them. They will know which cardinal direction the most food is in, where the most of their mates are, and where there are enemies. This will allow for exploration.

7. Cells also have a sense of the immediate convolutional world around them. The world looks like this to a cell:

```
####### X in center = cell (self)
#X   O# X in upper left = mate cell
#  X  # O in upper right = unmatable cell
#     #
#######
```

8. Cells will also be able to see the basic stats for each cell in its sight. This will allow for judgement of best mates, whether or not to attack, etc.

9. Cells also get information on the food on each cell in their sight.

10. Cells can only aid in attacks if the same enemies are in their sights.

11. Cells will attack the closest and then weakest cell if it decides to attack and there are multiple unmatable cells in its sight.

12. Cells can choose to: [Move up, move down, move left, move right, attack, eat, mate]

13. Two cells have to mate on the same turn to reproduce. If more than two cells in the same sight mate, the two strongest cells mate and produce a baby.

14. Babies can be placed anywhere there is free space between the two parents. If there is no free space between the two parents, the mating will fail.

15. Babies use a genetic algorithm to recieve their genes.

16. If cells make no babie and die out, new life will be randomly spawned on the board via your subjective choice of primorial soup, amino acid comet, or god.
