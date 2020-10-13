# CS611 Project1 Steering Behaviors for controlling cars (Java)

 Company: Drexel University CS 611:Game AI

 Engineer: Cheng HONG - ch3283
 
 Sketch: This script is written to implement Steering Behaviors
 
 Date: 2020/06/01


## Environment

 Windows 10 (64bit)

 IntelliJ IDEA

 Jave version '15'
 
## Task

 SeekSceneario
 
 ArriveScenario

 WallAviodSeekScenario

## How to use

 Put the all the source in the same document, then you can display each scenario finding in Test Folder.

## What I do

1) Vectors class: Designed for basic vector's multiplication, addition, normalization, dot product. The reason I did this it becauses the Game object is based on a 2-D coordinate system.

2) Output filtering class: Designed for transforming the seek behaviors into the car steering behaviors, that's because we can only control the car in order to generate the acceleration, thus we need this filter.

3) Controllers.SeekController: This class is created to achive the seek algorithm for the target car. Basically, we define a ''Seek'' function





