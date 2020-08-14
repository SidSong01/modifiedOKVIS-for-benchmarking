# Modified OKVIS
---

Modified the OKVIS source code for outputing the trajectory in a .txt file

the modifications is in the \okvis\okvis_apps\src\okvis_app_synchronous.cpp

the purpose of it is for evaluating and comparing the performace of different Visual odometry algorithms.

the evaluation tool: https://github.com/MichaelGrupp/evo

## The output trajectory is in .txt file with tum data format.
---

((time, t x , t y , t z , q x , q y , q z , q w ))

* Each line in the text file contains a single pose.
* The format of each line is 'timestamp tx ty tz qx qy qz qw'
* timestamp (float) gives the number of seconds since the Unix epoch.
* tx ty tz (3 floats) give the position of the optical center of the color camera with respect to the world origin as defined by the motion capture system.
* qx qy qz qw (4 floats) give the orientation of the optical center of the color camera in form of a unit quaternion with respect to the world origin as defined by the motion capture system.

### See the `trajectory_01.txt` for a sample review.

This is the output from the euroc dataset, mh01, in tum format.

## How to run the okvis
---

Please refer to the original repository.

## How to run the monocular version of OKVIS
---

Modify the config file in okvis--comment one of the camera calibartion infomation, then it will run the monocular version.

## Example for running stereo and monocular okvis in euroc dataset.

![image](https://github.com/SidSong01/modifiedOKVIS/blob/master/example.png)

## Example for the evaluation results

This is the exampel on Main Hall 01 dataset, more functions of the evaluation tool can be found in [evo](https://github.com/MichaelGrupp/evo).

The comparision betweent the different algorithms, other results like RMSE, Std, etc., can alos be abtained.

![image2](https://github.com/SidSong01/modifiedOKVIS/blob/master/MH_01.png)


![image2](https://github.com/SidSong01/modifiedOKVIS/blob/master/RMSE.png)

```
dataset is the euroc mh01
```

