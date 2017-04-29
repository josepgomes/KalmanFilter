# KalmanFilter
KalmanFilter is a simple and small library that can be easily called in your c++ project without any dependency.

## Some Results

### Before Kalman Filter
![Data Without Kalman Filter](/resources/b1before.png?raw=true "Data Without Kalman Filter")

### After Kalman Filter
![Data Without Kalman Filter](/resources/b1after.png?raw=true "Data Without Kalman Filter")

## Installation

There are no dependencies, pure math! Just add KalmanFilter.h to your project and don't forget to add #include "KalmanFilter.h".

## Using

Using the library is easy.

```c
//Measurements
float values[11] = {79,76,77,81,95,85,86,95,80,83,86};

//KalmanFilter(Process noise, Measurement noise, State vector, Control vector, Measurement vector);
KalmanFilter kalmanFilter = KalmanFilter(0.01, 3, 1, 0, 1);

for (int i = 0; i < 11; i++)
{
  //kalmanFilter.filter(Measurement, Control);
  printf("%f ", kalmanFilter.filter(values[i], 0));
}

//output
//79 77.4975 77.3307 78.2587 81.6734 82.2446 82.8041 84.416 83.889 83.7919 84.0154
```
