# Extended Kalman Filter Project


In this project a kalman filter is implemented to estimate the state of a moving object of interest with noisy lidar and radar measurements.

An overview of the Kalman Filter Algorithm is shown below:

![Kalman_Filter_Overview](data/Kalman_Filter_Overview.png)
Source: Udacity

If it is the first measurement (either from Lidar or radar), the state and covariance matrices are initialized. The predict step of the Kalman filter is the same for the Lidar and the radar.

In the update step of the Kalman filter, the filter compares the predicted location with the sensor measurement. The predicted location and the measured location are combined to give an updated location. When another sensor measurement is received after a time period t, the algorithm performs another predict and update operation.

To evaluate the performance of the Kalman Filter, the root mean square error (RMSE) is also calculated in the file tools.cpp in a fuction CalculateRMSE.
