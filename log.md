# 100 Days Of Code - Log

### Day 7: January 11, 2017

**Today's Progress**: Changed the GUI so that the robot parameters are entered in / changed / saved via a pop-up window rather than on the main screen as they aren't changed often. I then changed from having the text entry boxes as where I stored the values during run time, as I realised this was dangerous and limiting, to a dictionary.

**Thoughts:** Was interesting finally using a dictionary for a useful purpose after always seeing it demonstrated in python tutorials because before I never really saw it being useful in production.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/a0cc97c867ad1ca23a60346a7e7d7684dfc0216a)


### Day 6: January 10, 2017

**Today's Progress**: Added proximity sensor positions to the robot config parameters and GUI. Added the current control state to the GUI.

**Thoughts:** I think it will be more useful to have the robot parameters/config on a seperate pop-up for when needed as it doesn't need to be accessed as much. Instead, I'd like to put the controller PID parameters on the main GUI screen so that they can be easily changed and tested. On reflection, this was what I originally planned for the GUI changes, but got side-tracked on the robot parameters.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/0c7a58d5dae1c6099fb2019c90bc930be490c748)


### Day 5: January 9, 2017

**Today's Progress**: Added proximity sensor parameters to the robot config parameters and save/load function. Modified the way parameters are added by sorting them into dynamically created tables. The tables and parameters they contain are named with number ID so that the parameters and GUI can be more easily changed in the future.

**Thoughts:** Missed a day of coding yesterday due to busy weekend. Hopefully back on track now and I'll keep getting this GUI worked out. I need to be careful I don't get stuck adding to the GUI for too long. I think I might move onto updating the comms to the robot and reading the sensor values later this week.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/e463cc7a42cd69c308ff95d68468f8c31ac214cd)


### Day 4: January 7, 2017

**Today's Progress**: Added the robot's physical dimensions to the robot config parameters and save/load function. Modified the parameter add function so that it's more generic for adding and accessing the parameters.

**Thoughts:** Learnt about the power of setattr and getattr for creating objects dynamically, which is really really useful.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/4ed30ded1c36ae81e40560eb44dca9f46028b72b)


### Day 3: January 6, 2017

**Today's Progress**: Added save and load buttons so that the robot parameters listed in the GUI can be saved and loaded to quickly change the robot in the simulator. I also updated the UML file for the project to correctly reflect the current class structure of the code.

**Thoughts:** Making good progress on the project, the save and load buttons were surprisingly easy to setup by copying the code for the map save and load. I updated the UML so that I can have a clearer picture of what class should connect to what, so I don't create a birds nest by accident. Next step is to add all the robot parameters to the GUI, as I'd like to get the GUI finished before proceeding onto integrating the robot's sensors properly.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/c84dbfd14b3ab5894e3692efac1aedc178941d96)


### Day 2: January 5, 2017

**Today's Progress**: Added text input boxes for the robot's physical parameters to the robot configuration parameters section of the GUI. If these parameters are changed in the GUI, the robot is loaded with the new values when the simulation is reset. 

**Thoughts:** I'd like to add all the other parameters for the simulator that I currently have as constants in the simulator code to input boxes on the GUI. Then I'd like to save these values and load them from a file. This will be handy for quickly adapting the simulator for different robots.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/d2eea4da3505cd796588140cd03b5e6b9d21285c)


### Day 1: January 4, 2017

**Today's Progress**: Fixed step and pause button, added area to GUI for robot configuration parameters

**Thoughts:** Back working on my Pass the Butter robot software. It's good to get back into this project after a long break, hopefully I can keep momentum this time.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/821afdc9dd8737cd609c389d07cc5b0c9f9ec679)
