# Project 2_0: Introduction to Robotics with Java
This assignment will have you first create a WPILib Project and then have write your first WPILib program in Java to control a motor.  

***Pre-req:***

- Must have set up your environment in [Project 0_1](https://classroom.github.com/a/d-9tQmrq)
- Must have motor ID's in [Project 1_0](https://classroom.github.com/a/uBMaL_y6)

## ***Project Creation***

- Hit `ctrl + p` (`cmd + shift + p` on mac) to open up the command palette
- Type `Create a new project` and hit enter

<img src="images\newproject.png" alt="drawing" width="1000"/>

***right click on image and click open image in new tab to view a bigger version of what to fill in***

- Fill out the Project Creator so it looks something like above.
	- Chose which ever folder you want your project to be made in
	- The project name should indicate what year it is, the project should also be in pascal case. (e.g. `2022-SomeNamePascalCase`)
	- Type 3647 for the team number. You will not be able to deploy code to the robot if your have the wrong team number. 
- Click `Generate Project`. After this, a terminal should pop up at the bottom of your screen. 

***In about 35 seconds, your terminal sound read `BUILD SUCCESSFUL`***

### ***File Structure Adjustment***
***Current Default File Structure***
```
java
└── frc
    └── robot
        ├── commands
        │   └── ExampleCommand.java
        ├── Constants.java
        ├── Main.java
        ├── RobotContainer.java
        ├── Robot.java
        └── subsystems
            └── ExampleSubsystem.java
```

***Note: all folder names should be lower cased***

- Go into the java folder of your project through vscode or through file explorer
- Inside of the `java` folder, create a folder called `team 3647`
- Inside of the `team3647` folder you just made, create a folder called `frc2022` (or whatever year it is) and `lib`
- Inside of `frc2022`, add
	- autonomous
	- commands
	- inputs
	- robot
	- subsystems
- Move `Main.java`, `Robot.java`, and `RobotContainer.java` into team3647/frc2022/robot
- Delete the frc folder
- remove all import statements from ```RobotContainer.java```
- return null in getAutonomousCommand() in ```RobotContainer.java```

***Make appropriate edits to the package statements at the top of these files***

***Final Adjusted File Structure***
```
java
└── team3647
    ├── frc2022
    │   ├── autonomous
    │   ├── commands
    │   │   └── ExampleCommand.java
    │   ├── constants
    │   │   └── Constants.java
    │   ├── robot
    │   │   ├── Main.java
    │   │   ├── RobotContainer.java
    │   │   └── Robot.java
    │   └── subsystems
    │       └── ExampleSubsystem.java
    └── lib
```

### ***Modify build.gradle***
modify this line on build.gradle from:
```
def ROBOT_MAIN_CLASS = 'frc.robot.Main'
```
to 
```
def ROBOT_MAIN_CLASS = 'team3647.frc2022.robot.Main'
```

This is because the path to your `Main.java` file has changed after you adjust your file structure according to the instructions above. 

### ***Build Code***
- Hit `ctrl + p` (`cmd + shift + p` on mac) to open up the command palette
- Type `build` and press enter for `WPILib: Build Robot Code`
- If all has been done correctly, the terminal should say `BUILD SUCCESSFUL` in about 30 seconds

## ***Robot Code Requirements***
***Project Name: `2022-Project2_0`***

- Double check, triple check that the motor you are running is the correct motor for the correct ID. Do not run code without double checking, otherwise you maybe spinning the arm or the turret at very dangerous speeds. 
- Create a FalconFX object with the ID corresponding to a motor on the intake of the 2022 robot in Robot.java
- Create a TalonSRX object with the ID corresponding to a motor on the intake of the 2018 or 2019 robot in Robot.java
- Spin motor at a constant 0.3 percent output and then try spinning the motor at the same speed in the opposite direction. 
	- Hint: write this in teleopPeriodic()

## ***Authors***
- [Team 3647, Edward Sun](https://github.com/EdwardoSunny)












