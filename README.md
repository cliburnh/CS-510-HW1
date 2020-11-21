# CS611 Project4 Strategic Decision Making in microRTS (Java)

 Company: Drexel University CS 611: Game AI

 Engineer: Cheng HONG - ch3283
 
 Sketch: This script is written to implement Strategic Decision Making
 
 Date: 2020/11/21

## Environment

 Windows 10 (64bit)

 IntelliJ IDEA

 Jave version '15'
 
## Task

 a knowledge-base, an inference engine and simple-rules-base.

## How to use

 Put the all the source in the same document, then you can make the game run by changing the path of rules as yours in the file ai.abstraction.LightRush, as follow:
 ```java
 String pathname = "C:\\Users\\cliburn\\Desktop\\microrts-master\\src\\ai\\abstraction\\simple";
 ```
 Also, you can choose the AI you want to use, edit the file test.GameVisualSimulationTest as follow:
 ```java
 // AI ai1 = new MouseController(w);
 // AI ai1 = new PassiveAI();
 // AI ai1 = new RandomBiasedAI();
    AI ai1 = new LightRush(utt, new AStarPathFinding());
 ```

## What I do
 
 In this project, we need to work in a RTS S3 Game and Implement the A* algorithm to reliaze a pathfinding function. In order to achieve this, firstly I need to design a proper  coordinate to represent each state(location). Then we need a check state function to distinct each location. Also, I use a hashmap to record each branch of node for the A* algorithm. In the A* part, I use a hashmap to recode F in each cell. Thus, this algorithm can be simply achieved by check the lowF cell each time.

1) Manhattan function: Designed for computing the Manhattan Distance.

2) checkState function: Designed for testing if the object have arrived the destination.

3) compareState function: Designed for testing if the object have already check this location, if have arrived once then ignore this location.
  
4) nextPossibleLocation function: This function is create to check if a cell in the map is free, I use the function "anyLevelCollision" of the S3 class here.
   
5) AStar function: Return the nearest way from the current location to destination.

 Also, I find a simple way to achieve the system by adjust the class of node except using hashmap. We can add the attributes of parental node for each node, and also the Attributes of F. It will be more readable. Besides, using prime number for each location of node can help the A* algorithm run faster.
   
