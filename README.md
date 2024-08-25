# Open-Source-Kinematic-Analysis-Toolkit
A free and open-source toolkit has been developed using an anthropomorphic arm model. It allows any data set containing joint angles over time to be implemented to visualise motion for kinematic analysis.

Welcome to my MRes dissertation project.
This repository contains the following:

-Simplified Arm model

-Code for simulation

-Link to Participant-generated joint angles: https://github.com/MiaH-kin/UE_ADLdatabase/tree/master

-Packages used in conda environment 

1.	Use Anaconda to create a virtual environment 
2.	Download “environment.yml” to local machine
3.	Run the following line in anaconda prompt:
a.	conda env create --file /path/to/environment.yml
i.	Replacing “/path/to/environment.yml” with the path to the file
4.	Activate the environment using the following command:
a.	Conda active sim_env
5.	Verify packages by comparing results produced from this line with the txt file “requirements.txt”:
a.	Conda list
6.	Lines 421-428 contain the paths to the participant files, please change them accordingly to where they are currently installed on your machine 
a.	"*where you saved project too*/Dissertation_Code/Joint Angles/UE_ADLdatabase-master/ADL004/ADL004FR1angles.csv"
7.	By default, the model is performing one of the participants reaching forward motion visualised by the GUI that pops up
8.	Additionally, all kinematic information will be presented once the simulation has run its course, but to see the next, the first will need to be closed, not the GUI.
a.	Please note that the kinematic workspace will take time to run 
9.	If you wish to change which participant data is being used by the model, you will find this nested in the function real_data()
a.	Look for the current data and comment/uncomment which one you would like
b.	Please note that the file path will need to be verified 
10.	If you wish to change the movement being performed for it to be manual movement, you will need to change two things:
a.	The first is in the function Bicep_curl, the majority of the code will need to be uncommented so that you can see which block of code performs which movement
b.	The second is in the main() function you will need to comment out the real data function and uncomment the line that begins with “joint_positions_timeline….” I have left a comment below which line
c.	” 
11.	In the Anaconda prompt terminal, run the following command
a.	Python testing.py
b.	This will run the simulation


### Table One: Value Key for Movements for each Joint 

| Joint     | Movement              | Positive | Negative |
|-----------|------------------------|----------|---------|
| Shoulder  | Flexion                |          |   YES   |
| Shoulder  | Extension              | YES      |         |
| Shoulder  | Internal Rotation      | YES      |         |
| Shoulder  | External Rotation      |          |   YES   |
| Shoulder  | Abduction              | YES      |         |
| Shoulder  | Adduction              |          |   YES   |
| Elbow     | Flexion                |          |   YES   |
| Elbow     | Extension              | YES      |         |
| Wrist     | Pronation              | YES      |         |
| Wrist     | Supination             |          |   YES   |
| Wrist     | Flexion                | YES      |         |
| Wrist     | Extension              |          |   YES   |
| Wrist     | Ulnar Deviation        |          |   YES   |
| Wrist     | Radial Deviation       | YES      |         |




