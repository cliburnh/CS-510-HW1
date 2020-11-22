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

 a knowledge-base, an inference engine and simple-rules-base system.

## How to use

 Put the all the source in the same document, then you can make the game run by changing the path of rules as yours in the file ai.abstraction.LightRush, as follow:
 ```java
 String pathname = "C:\\Users\\cliburn\\Desktop\\microrts-master\\src\\ai\\abstraction\\simple";
 ```
 Then, set the test.PlayGamewithMmouseTest as the main class.
 Also, you can choose the AI you want to use, edit line 40~44 in the file test.PlayGamewithMmouseTest as follow:
 ```java
 // AI ai1 = new MouseController(w);
 // AI ai1 = new PassiveAI();
 // AI ai1 = new RandomBiasedAI();
    AI ai1 = new LightRush(utt, new AStarPathFinding());
 ```

## What I do
 
 In this project, we need to work in a microRTS platform in order to achieve Strategic Decision Making module. To begin with, we need to percept a Knowleadge Base by detecting all units in the map. Then we should read the rules stored in the txt.file. After translating the rules from words to code, a inference system has been implemented to accomplish the rule-order. In order to achive these function, 4 main functions has been written as follow:

1) getKB function: Return HashMap List stored Knowleadge Base, designed for summarizing the environment variables and pacakege them.

2) readRules function: Return String List, designed for reading txt. rules file from specific path.

3) transRules function: Return HashMap List, designed for translating rules into Knowleadge Base forms.
  
4) inference engine part: Extend the getAction(), this part is created to unificate the rules and Knowledage base, also excute the FiredRules.
   
 Also, for the future work if we want to achieve higher-oder rules like rules-complex.txt, we can improve the transRules function in order to have a better libaray to transforlate more keywords.
   
