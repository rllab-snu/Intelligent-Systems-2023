# Intelligent-Systems-Project

## Start Intelligent Systems Project

```
$ cd ~/catkin_ws/src
$ git clone https://github.com/rllab-snu/Intelligent-Systems-2022.git
$ cd ~/catkin_ws && catkin_make
```

If you don't remove preproject folders, you would have some conflicts. Also, we recommend delete /devel and /build folders before compiling catkin workspace.

```
$ cd {DIR_sim2real}/project
$ git clone {YOUR_TEAM_REPOSITORY}
$ cd IS_{TEAM_NAME} && mkdir project
$ cp ../RLLAB/project/RLLAB_project1.py project/{TEAM_NAME}_project1.py
```

Copy the skeleton code to your repository and implement TODO parts. {YOUR_TEAM_REPOSITORY} should be named IS_{TEAM_NAME}.

```
$ cd {DIR_sim2real}
$ vi CMakeLists.txt  # then change the value of TEAM_NAME
$ cd ~/catkin_ws && catkin_make
```

Please change TEAM_NAME in CMakeLists.txt and recompile the packages.


## Evaluation your code (Project1)
```
$ roslaunch sim2real base_p1.launch
```

Open another terminal, then execute the below command.

```
$ rosrun sim2real {TEAM_NAME}_project1.py
```

Finally, you open one more terminal, and publish topic manually.

```
$ rostopic pub /query sim2real/Query "{id: '0', trial: 0, name: '{TEAM_NAME}', world: 'track_1', exit: false}"
```

## Evaluation your code (Project2)
```
$ roslaunch sim2real base_p1.launch
```

Open another terminal, then execute the below command.

```
$ rosrun sim2real {TEAM_NAME}_project2.py
```

Finally, you open one more terminal, and publish topic manually.

```
$ rostopic pub /query sim2real/Query "{id: '0', trial: 0, name: '{TEAM_NAME}', world: 'track_1', exit: false}"
```
## Evaluation your code (Project3)

```
$ roslaunch sim2real base_p3.launch
```

Open another terminal, then execute the below command.

```
$ rosrun sim2real {TEAM_NAME}_project3.py
```

Finally, you open one more terminal, and publish topic manually.

```
$ rostopic pub /query sim2real/Query "{id: '0', trial: 0, name: '{TEAM_NAME}', world: 'track_1', exit: false}"
```

## Map Building for Project 3

For basic map building instructions, please refer to the map building tutorial uploaded on ETL.

If you wish to create your own project 3 world with your created maps, you can make it by typing the following command.

```
$ roscd sim2real/scripts
$ python eval_generator.py
```

If you have any questions, please contact to TAs or use repository issue.

