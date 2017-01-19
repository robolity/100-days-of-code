# 100 Days Of Code - Log

### Day 13: January 19, 2017

**Today's Progress**: Modified the Zumo arduino code so that the encoder values are printed to the LCD. I then verified that the encoder readings being split into chars to send via serial are successfully received as char values that when combined match the decimal encoder reading on the robot.

**Thoughts:** The encoder readings recieved by the simulator are one cycle behind  being read by the robot. I need to investigate if there is a way of fixing this.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/f11600d6674e3f896a9d10c17559c884d36a2279)


### Day 12: January 18, 2017

**Today's Progress**: Added the function to RobotPhysicalInterface and the Zumo arduino code to request and receive the encoder values. The communication stream is working, but the simulation still freezes and synchronising the serial calls and reads needs a lot of improvement.

**Thoughts:** Nice to start working with my robot again, and mixing hardware with software. I need to work out the most efficient way of reading the encoder values each step, and how to then use them correct the wheel velocities sent to the robot to keep it matching the simulation.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/f11600d6674e3f896a9d10c17559c884d36a2279)


### Day 11: January 17, 2017

**Today's Progress**: Updated RobotComm class to be a bit more efficient. These changes were from another serial comms project I worked on, and there is still some more integration and testing to be done. Also, I added a world time counter to the GUI.

**Thoughts:** The simulator is sending commands to my physical Zumo robot, but the simulation freezes after about 2.5s, and if I pause it, the simulator catches up. I think the stream of serial send commands are clogging up the processing for the simulator, so I'm going to work on doing this on a need to basis maybe? Not sure what the best approach will be, but that's the kind of learning this project is all about :)

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/411ee78a850f58093abc4bc794ed5cc8c6db96fa)


### Day 10: January 16, 2017

**Today's Progress**: Fixed the link between changing the text entry boxes and assigning them to the internal parameter list, as well as applying loaded config parameters to the tect entry boxes. Also, the Apply buttons are greyed out until the text entry boxes are changed.

**Thoughts:** Now I've finished with GUI changes for now, time to work on interfacing the physical robot prox and encoder sensors.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/48ddc35835a67c1385ec8d6d699ca1a468c4dff5)


### Day 9: January 15, 2017

**Today's Progress**: Added the control settings for the controllers to the main GUI screen so that these can be quickly changed during simulation to fine tune the motion of the robot.

**Thoughts:** Almost finished with GUI changes, I'll move onto comms to the physical robot prox and encoder sensors later this week.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/23d8ec20e704afe3e9695753927f3ac52039665f)


### Day 8: January 14, 2017

**Today's Progress**: Finalised the robot parameters pop-up window and saving changes to the text entry boxes to a list of the parameters. Discovered that the avoid obstacles controller wasn't working because it doesn't react to obstacles if it approaches the obstacle's corner.

**Thoughts:** Missed 2 days of coding, and struggling to keep momentum every day. I think to penalise this I'll make it that I have to do catch up days. These will be 1hr+ sessions that complete one of the daily milestones I set. This way hopefully I'll keep the progress on track and keep the challenge alive. Also, realised the way I was using the dictionary was not right for the application as it's more efficient to reference the parameters and tables by an iterable number reference.

**Link to work:** [Pass the Butter](https://github.com/robolity/pass-the-butter/commit/e61d936d461917474515a52c8abac5aa63201855)


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
