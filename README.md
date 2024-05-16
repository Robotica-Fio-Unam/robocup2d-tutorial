# RoboCup2D Soccer Simulation Tutorial (NOT OFFICIAL)

> :warning: **DISCLAIMER** :warning:
> 
> These tutorials are not official and some sections are still missing.
>
> I created this repo while I was part of a Simulation 2D team at university. There was only Japanese guides at that time and I wanted to organize all the information I could gather and share with other developers.
>
> There's no guarantee that everything will work fine on your OS. Please, be advised!
>
> For the official RoboCup 2D guide and source code, go to https://rcsoccersim.github.io/ and https://github.com/rcsoccersim.

This repository contains a series of tutorials on the RoboCup2D Soccer Simulation Tutorials. The tutorials cover several topics such as installation, soccer server and the libraries librcsc and agent2d.

This tutorial is live here: https://herodrigues.github.io/robocup2d-tutorial

# Overview

**NOTE**:
- It is preferable to use your Linux distribution in English. Some problems were reported when executing the simulator when the system language uses a comma as the decimal separator, for example, the Portuguese language.

### Articles  

- Tutorials
    - [Installing the simulator](sections/installing-the-soccer-simulator.md)
    - [Running a match with agent2d](sections/running-a-match-with-agent2d.md)
    - [Configuring the trainer](sections/configuring-the-trainer.md)
    - [Creating formations with fedit](sections/formations-with-fedit.md)

- Utility
    - [Autotools tutorial](sections/autotools-tutorial.md)
    - [Script to run server, monitor and teams simultaneously](sections/script-for-running-server-and-match.md)
    - [SoccerWindow2 as a debugger](sections/soccerwindow2-debugger.md)

- Team development
    - [Dynamic positioning](sections/dynamic-positioning.md)

**agent2D**
- Chain actions
    - [ActionGenerator](sections/ActionGenerator.md)
    - [ActionStatePair](sections/ActionStatePair.md)
    - [CooperativeAction](sections/CooperativeAction.md)
    - [FieldAnalyzer](sections/FieldAnalyzer.md)
    - [PredictState](sections/PredictState.md)
- Behaviours
    - [Bhv_BasicMove](sections/Bhv_BasicMove.md)
    - [Bhv_BasicOffensiveKick](sections/Bhv_BasicOffensiveKick.md)
    - [Bhv_BasicTackle](sections/Bhv_BasicTackle.md)
    - [Bhv_GoToStaticBall](sections/Bhv_GoToStaticBall.md)
- Roles
    - [Roles](sections/Roles.md)
- Others
    - [Strategy](sections/Strategy.md)

**librcsc**
   - Geometry
     - [AngleDeg](sections/AngleDeg.md)
     - [Line2D](sections/Line2D.md)
     - [Matrix2D](sections/Matrix2D.md)
     - [Ray2D](sections/Ray2D.md)
     - [Triangulation](sections/Triangulation.md)
     - [Vector2D](sections/Vector2D.md)
     - [Voronoi Diagram](sections/VoronoiDiagram.md)
   - Player
     - [BallObject](sections/BallObject.md)
     - [PlayerObject](sections/PlayerObject.md)
     - [PlayerAgent](sections/PlayerAgent.md)
     - [SoccerAction](sections/SoccerAction.md)
     - [Localization](sections/Localization.md)
     - [SeeState](sections/SeeState.md)
     - [InterceptTable](sections/InterceptTable.md)
   - Others
     - [MathUtil](sections/MathUtil.md)
     - [SoccerMath](sections/SoccerMath.md)
