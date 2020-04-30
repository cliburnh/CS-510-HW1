# CS510 HW1 Sliding Brick Puzzle

 Company: Drexel University CS 510

 Engineer: Cheng HONG - ch3283
 
 Sketch: This script is written for provding different solution in Sliding Brick Puzzle
 
 Date: 2020/04/29


## Environment

 Windows 10 (64bit)

 Python 3.7.6

 Jupter Notebook

## Item

Radom Walk, BFS, DFS ,IDS and A* algorithm

Output-hw1.txt in each algorithm and 4 SCP level

HW1.py and HW1.ipynb

## How to use
Choose value of Method and Maze to see the result:

```python
N = 3                # Random walk step

Flag_RandomWalk = 0  # Set value = 1 to choose method
Flag_BFS = 0
Flag_DFS = 0
Flag_IDS = 0
Flag_AStar = 0

Flag_Maze = 0        # You can choose 0, 1 ,2 or 3 which represent the level of SBP
```

For example, if I wanna use BFS and SBP-level0:

```python
Flag_BFS = 1         # Set Flag_BFS = 1
Flag_Maze = 0        # Choose Flag_Maze = 0
```

and we can get output:
```python
[2, 'left']
[4, 'down']
[3, 'right']
[2, 'up']
[2, 'up']
[5, 4]
[1, 2, 2, 1, 1]
[1, 0, 0, 3, 1]
[1, 0, 0, 4, 1]
[1, 1, 1, 1, 1]
#16 0 seconds and 0/100 5
```
To be noticed, the last line represent #nodes time length

## All Algorithms are Completed!
