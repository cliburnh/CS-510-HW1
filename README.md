# CS611 Project1 Steering Behaviors for controlling cars (Java)

 Company: Drexel University CS 611:Game AI

 Engineer: Cheng HONG - ch3283
 
 Sketch: This script is written to implement Steering Behaviors
 
 Date: 2020/10/13


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

3) SeekController: This class is created to achive the seek algorithm for the target car. This class receive two car object and calcuate the acceleration vector for seeking by      imploit the location of these car.
   Basically, we define a ``seek()`` function which follows the formulas in lecture:
   ```
   Seek(character, E)
   D = E - character.position
   ND = D / |D|
   A = ND * maxAcceleration
   Return A 
   ```
   After finding the accleartion vector, we can use the Output filtering to control the car.
  
4) ArriveController: This class is create to achive the arrive algorithm for the aimed location. This class also receive two car object and calcuate the acceleration vector for    seeking by imploit the location of these car, besides this class also define a targetRadius for stopping and a slowRadius for slowing down.
   Basically, we define a ``arrive()`` function which follows the formulas in lecture:
   ```
   Arrive(character, E, targetRadius, slowRadius, time)
   D = E - character.position
   Length = |D|
   If Length<targetRadius Return (0,0,0)
   If Length>slowRadius then targetSpeed = maxSpeed
    else targetSpeed = maxSpeed * Length/slowRadius
   targetVelocity = (D/|D|)*targetSpeed
   A = (targetVelociy – character.velocity)/time
   If |A|>maxAcceleration then A = (A/|A|)*maxAcceleration
   Return A 
   ```
   After finding the accleartion vector, we can use the Output filtering to control the car.
   
5) ArriveControllerAdvanced: This class is create to achive the avoid algorithm for the wall. This class also receive two car object and calcuate the acceleration vector for        seeking by imploit the location of these car, besides this class need a ``findObstacle()`` function in order to locate the wall and adjust the acceleration to flee away from    the obstacle.

   In addition, we define ``locateNew()`` and ``seekNew()`` function to locate and seek a new target when the oder target will cause a collision.
   
