# modifiedOKVIS

modified the OKVIS source code for outputing the trajectory in a .txt file

the modifications is in the \okvis\okvis_apps\src\okvis_app_synchronous.cpp

the function of this is for evaluating the performace.

the evaluation tool: https://github.com/MichaelGrupp/evo

# the output trajectory is in .txt file with tum data format.

((time, t x , t y , t z , q x , q y , q z , q w ))

# see the trajectory_01.txt

this is the output from the euroc dataset, mh01

# for running the okvis

please refer to the original repository.

# for running the monocular version of OKVIS

modify the config file in okvis--comment one of the camera calibartion infomation

# example for running stereo and monocular okvis in euroc dataset

![image](https://github.com/SidSong01/modifiedOKVIS/blob/master/example.png)
