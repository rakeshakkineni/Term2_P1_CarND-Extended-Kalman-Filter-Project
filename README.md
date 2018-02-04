# Extended Kalman Filter Project

## **Extended Kalman Filter Project**

The goals / steps of this project are the following:
* Modify the code to estimate the vehicle position and velocity using LIDAR data
* Add code such that even RADAR data is used for estimating the vehicle position and velocity


[//]: # (Image References)

[image1]: ./Output/Graphical_Image.png 
[image2]: ./Output/Px_RMSE.png 
[image3]: ./Output/Py_RMSE.png
[image4]: ./Output/Vx_RMSE.png
[image5]: ./Output/Vy_RMSE.png


---
### Writeup / README
In this project simulated RADAR and LIDAR data is used to estimate Vehicle position and Velocity using Extended Kalman Filter. Source code provided by "UDACITY CarND Extended Kalman Filter" was used as base for this project. 

### Modifications
FusionEKF.cpp , kalman_filter.cpp , tools.cpp are modified to implement fusion logic. Predict , Update , UpdateEKF functions were modified to proces RADAR/ LIDAR data. CalculateRMSE function was also modified to calculate RMS value.

### Code Flow
Following is brief description of the flow of the code.
- Initialize the Kalaman Filter. 
- Establish the connection with simulator.
- Get the data from the simulator for one scan.
- Perform Perdict the future position and velocity of the vehicle.
- Check if the data is from LIDAR or RADAR, accordingly call Update or UpdateEKF functions.
- Calculate the RMSE for each of the parameters and send it to Simulator and print it to a file.

### Output
Kalman Filter was able to estimate the position of the vehicle. 

-In the following picture the estimated path followed by the vehicle is in green. 

[image1]

- RMSE for each scan is printed in a text file. Using the printed data graphs were ploted to understand the trend of the RMSE for each parameter. 

[image2]

[image3]

[image4]

[image5]
