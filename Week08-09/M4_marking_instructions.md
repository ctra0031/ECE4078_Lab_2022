# M4 Marking Instructions 
You will need to demonstrate your navigation and planning module in both the simulation and the physical robot during the Week 10 lab session.

**Please familiarise yourselves with these steps to ensure the demonstrators can finish marking your team in the allocated time**
- [In-person marking steps](#in-person-marking)
- [In-person marking checklist](#in-person-marking-checklist)
- [Zoom marking steps](#zoom-marking)
- [Zoom marking checklist](#zoom-marking-checklist)

Each team will have a **STRICT** time limit get marked, 20min for the simulator demo and 10min for the physical robot demo, according to this [marking schedule](https://docs.google.com/spreadsheets/d/14GB1km85aYwIS4eiDUr7CUI0OCfg7yIZ2AUgJ6iAMlA/edit?usp=sharing). You may open up the marking checklist, which is a simplified version of the following steps to remind yourself of the marking procedures. You MUST follow all the rules outlined in the [marking scheme](README.md#marking-schemes), make sure you check out all the rules and understand all of them. 

**Note:** For the remote students (Lab 6), you will only need to demonstrate yours in the simulator.

### In-person marking
#### Step 1:
**Do this BEFORE your lab session**
Zip your **whole Week08-09 and catkin_ws folders** (see the picture below) to the Moodle submission box (according to your lab session). Each group only needs one submmission. This submission is due by the starting time of the lab session, which means you should **submit your script BEFORE you come to the lab**. 

**Tips:** 
- You may also include a text file in the zip file with a list of commands to use, if you don't know all the commands by heart.
- **Please practise** the marking steps (eg. unzipping your code and running it) to ensure there are no issues during marking.


#### Step 2: 
**Do this BEFORE the demonstrator come to mark your team**

1. Close all the windows/applications on your Ubuntu environment

2. Use any team member's account to log in Moodle in the Ubuntu environment (VM/native/WSL2, whichever one you use) and nagviate to the M4 submission box, so that you are ready to download your submitted code when the demonstrator arrives

3. Have an **empty** folder named "LiveDemo" ready at the Ubuntu home directory, ie. it is at ```~/LiveDemo/```. This folder should remain open at all time during marking (Does not apply to WSL2 users)

4. Please calibrate your physical robot as soon as you receive yours

5. Connect back to eduroam/internet so that you are ready to download your submission from Moodle

#### Step 3:
**During marking**
Similar to M2, your simulation demo and physical demo will be marked separately. After you receive your robot in the beginning of the lab session, you may divide your team into two groups. One group can start preparing for the simulation demo, and the other group can start to calibrate the robot (**highly recommended especially if you have a different robot**). You will be allowed to copy the physical robot calibration files later on during marking. 

**Note**: You may attempt any level you want, and you should make it clear to the demonstrator which level you are attempting. Within the marking time limit (20min for sim, 10min for robot), you may have as many attempts as you want. The attempt with the highest score will be your final score. 

1. The demonstrator will release the maps ```M4_true_map_3fruits.txt```, ```M4_true_map_5fruits.txt``` and the ```search_list.txt``` via Slack in the beginning of the session. Note that each lab session will get a slightly different map, so there is no point sharing the map with people in the other lab session

2. When the demonstrator starts to mark you, download your submitted zip file from Moodle and unzip its content to the "LiveDemo" folder. 

3. Place the true maps inside the ```Week08-09``` folder. **For robot demo** place the robot calibration files in the ```/calibration/param``` folder

4. **[SIM ONLY]** Open a terminal and type ```source ~/LiveDemo/catkin_ws/devel/setup.bash```

5. **[SIM ONLY]** Launch the simulator with ```roslaunch penguinpi_gazebo ECE4078.launch```

6. **[SIM ONLY]** Spawn the map with ```rosrun penguinpi_gazebo scene_manager.py -l map.txt```
    - use [M4_true_map_3fruits.txt](M4_true_map_3fruits.txt) for Level 2
    - use [M4_true_map_5fruits.txt](M4_true_map_5fruits.txt) for Level 1 and 3
    
7. Open another terminal, or new tab in the existing terminal, navigate to the "Week08-09" folder and run your M4 script, [auto_fruit_search.py](auto_fruit_search.py) or whichever script you need for the your chosen level to attempt
    - you may take ```M4_true_map_3fruits.txt``` and ```search_list.txt``` as input files

8. For Level 1, you may enter as many waypoints as you want. For Level 2 or 3, you can only input a single command to start the autonomous search
    - You will receive zero score if we find out that you are teleoperating the robot

9. Repeat any level as many times as you want until the time limit

---

### In-person marking checklist
**BEFORE the lab session**
- [ ] Submit your code to Moodle

**BEFORE the marking**
- [ ] Close all programs and folders
- [ ] In Ubuntu, login Moodle and navigate to the submission box
- [ ] Open an empty folder named "LiveDemo" (located at ```~/LiveDemo/```)
- [ ] Calibrate the robot, then connect your Wifi back to eduroam/internet

**During the marking**
- [ ] Demonstrator will ask you to download your submission and unzip it to "LiveDemo"
- [ ] Copy the true maps or the calibration files [ROBOT] to the "Week08-09" folder 
- [ ] **[SIM ONLY]** ```source ~/LiveDemo/catkin_ws/devel/setup.bash```
- [ ] **[SIM ONLY]** ```roslaunch penguinpi_gazebo ECE4078.launch```
- [ ] **[SIM ONLY]** ```rosrun penguinpi_gazebo scene_manager.py -l map.txt``` (depends on your chosen level)
- [ ] run your fruit search script
- [ ] enter as many waypoint as you want for level 1, but only a single command for level 2 or 3

---
### Zoom marking
#### Step 1:
**Do this BEFORE your lab session**
Zip your whole Week08-09 and catkin_ws folders (see the picture below) to the Moodle submission box (according to your lab session). Each group only needs one submmission. This submission is due by the starting time of the lab session, which means you should **submit your script BEFORE you come to the lab**. 

- You may also include a text file in the zip file with a list of commands to use, if you don't know all the commands by heart.
- **Please practise** the marking steps (eg. unzipping your code and running it) to ensure there are no issues during marking.


You will also need to install ```screenkey``` in  your Ubuntu. You can do so with ```sudo apt-get install screenkey```. We use this software to monitor your key press event. You can try this out by typing ```screenkey``` in the terminal, and then just type something. A bar should show up at the bottom of your screen showing what keys you have pressed. You can stop screenkey with this command ```pkill -f screenkey```.


#### Step 2: 
**Do this BEFORE the demonstrator come to mark your team**

1. Close all the windows/applications on your Ubuntu environment

2. Use any team member's account to login Moodle in the Ubuntu environment (VM/native/WSL2, whichever one you use) and nagviate to the M4 submission box, so that you are ready to download your submitted code when the demonstrator arrives

3. Have an **empty** folder named "LiveDemo" ready at the Ubuntu home directory, ie. it is at ```~/LiveDemo/```. This folder should remain open at all time during marking (Does not apply to WSL2 users)

4. If you have a dual monitor setup, please disconnect one of them. You are only allowed to use a single monitor during marking

#### Step 3:
**During marking**

**Note**: You may attempt any level you want, and you should make it clear to the demonstrator which level you are attempting. Within the marking time limit (20min), you may have as many attempts as you want. The attempt with the highest score will be your final score. 

The demonstrator will release the maps ```M4_true_map_3fruits.txt```, ```M4_true_map_5fruits.txt``` and the ```search_list.txt``` via Slack in the beginning of the session. Note that each lab session will get a slightly different map, so there is no point sharing the map with people in the other lab session

1. Please make sure only one display is used during the live demo. You will be asked to show your display setting with:
- Windows: Settings -> System -> Display
- Linux: xrandr | grep connected | wc -l (type this in terminal and then count the lines returned)
- Mac: System Preferences -> Displays

2. When the demonstrator starts to mark you, download your submitted zip file from Moodle and unzip it to the "LiveDemo" folder

3. Open a terminal and type ```screenkey```

4. type ```source ~/LiveDemo/catkin_ws/devel/setup.bash```

5. Launch the simulator with ```roslaunch penguinpi_gazebo ECE4078.launch```

6. Spawn the map with ```rosrun penguinpi_gazebo scene_manager.py -l map.txt```
    - use [M4_true_map_3fruits.txt](M4_true_map_3fruits.txt) for Level 2
    - use [M4_true_map_5fruits.txt](M4_true_map_5fruits.txt) for Level 1 and 3

7. Open another terminal, or new tab in the existing terminal, navigate to the "Week08-09" folder and run your M4 script, [auto_fruit_search.py](auto_fruit_search.py) or whichever script you need for the your chosen level to attempt
    - you may take ```M4_true_map_3fruits.txt``` and ```search_list.txt``` as input files

8. For Level 1, you may enter as many waypoints as you want. For Level 2 or 3, you can only input a single command to start the autonomous search
    - You will receive zero score if we find out that you are teleoperating the robot

9. Repeat any level as many times as you want until the time limit

---
### Zoom marking checklist
**BEFORE the lab session**
- [ ] Submit your code to Moodle
- [ ] Install ```screenkey``` in Ubuntu 

**BEFORE the marking**
- [ ] Close all programs and folders
- [ ] In Ubuntu, login Moodle and navigate to the submission box
- [ ] Open an empty folder named "LiveDemo" (located at ```~/LiveDemo/```)
- [ ] Only use a **single monitor** during marking

**During the marking**
- [ ] Show that you are only using a single monitor
- [ ] Demonstrator will ask you to download your submission and unzip it to "LiveDemo"
- [ ] Copy the true maps to the "Week08-09" folder
- [ ] Open a terminal and start ```screenkey```
- [ ] ```source ~/LiveDemo/catkin_ws/devel/setup.bash```
- [ ] ```roslaunch penguinpi_gazebo ECE4078.launch```
- [ ] ```rosrun penguinpi_gazebo scene_manager.py -l map.txt``` (depends on your chosen level to attempt)
- [ ] run your fruit search script
- [ ] enter as many waypoint as you want for level 1, but only a single command for level 2 or 3