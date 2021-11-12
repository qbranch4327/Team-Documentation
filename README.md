# Skills Day 1 - 2021
## Git and GitHub
**What is Git?**  
Git is version control software. It allows us to track changes to documents over time, see who made those changes, revert those changes, collaborate with others on the same set of documents, compare documents via diff, and more.

**What is GitHub?**  
Github is just git in the web. It allows you to easily collaborate with other people by providing a central remote repository that everyone on a project can copy and check into.

**How it all works**  
GitHub serves as the main repository. Anyone who wants to contribute to a project on GitHub can `clone into that project's repository`.  
    
After that, you may edit files however you wish without fear of breaking anything. Your copy is local to your computer. Generally, when you edit files in a project you'll want to create a `branch` for your feature. Branches allow you to isolate changes, making it much easier for teams to work on the same code base together.
  
When you are satisfied with your work, you need to `stage`, `commit` and then `push` your changes back up to the remote repo on GitHub. After that, you can create a `Pull Request` (or `PR`) to merge your changes back into the main branch.  

## Robot code concepts
[**Subsystems**](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html)  
"*A subsystem is an abstraction for a collection of robot hardware that operates together as a unit*"  
  
Subsystems are how you give robots abilities, they are where the logic for the robot lives. This is where you could do things like:
- `read and respond to driver input`
- `turn motors on/off and set the speed`
- read information from sensors
- act on information from other subsystems
- augment driver input with sensor data (collision avoidance, aim assist, etc.)

[**Commands**](https://docs.wpilib.org/en/stable/docs/software/commandbased/commands.html)  
"*Commands are simple state machines that perform high-level robot functions using the methods defined by subsystems.*"

Commands are how we use the robot's abilities that we provide in the subsystems. Commands can be bound to buttons so that when a button is pressed, it's associated command is run.  Commands can also be 

press button -> execute command -> invoke code  

Commands can be broken into two main types: RunCommands and InstantCommands.  

A [run command](https://docs.wpilib.org/en/stable/docs/software/commandbased/convenience-features.html#runcommand) is a command that shouldn't be canceled and is intended to be used as a default command. Consider a drive command. You want this command to always be running and looking for driver input. This doesn't mean that the robot will always be moving, just that it will always be ready to respond to user input. 
  
An [instant command](https://docs.wpilib.org/en/stable/docs/software/commandbased/convenience-features.html#instantcommand) is useful for toggling the state of a subsystem. Perhaps your drivetrain subsystem has a faster "movement" mode for covering the field quickly and a slower "precision" mode for aiming/lifting/interacting. You could use an Instant command to toggle between these two modes.

[**WPILib**](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/index.html)  
In the world of software, a library is just a bunch of helpful code that other people wrote, which you can use in your own projects. WPILib is a library that makes it easy for us to write software that interacts with robotics hardware and peripherals.

[VictorSP](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/wpilibj/VictorSP.html)  
[XboxController](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/wpilibj/XboxController.html)  
[Imaging your roboRIO](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/imaging-your-roborio.html)

# Q Branch Documentation
## Our GitHub Team Page
https://github.com/qbranch4327
## Branch naming conventions
Branches should follow the format: [yyyy]/[mm]/[description]  
ex: 2021/11/add_autonomous_command