# L3_Project
Description: 

Simulate traffic in a city grid with vehicles, streets and intersections. Vehicles drive around randomly and change direction at each intersection. Each object in the city grid will run independently in its own thread.

Project Tasks
- Task L3.1 : In class WaitingVehicles, safeguard all accesses to the private members _vehicles and _promises with an appropriate locking mechanism, that will not cause a deadlock situation where access to the resources is accidentally blocked.

- Task L2.2 : Add a static mutex to the base class TrafficObject (called _mtxCout) and properly instantiate it in the source file. This mutex will be used in the next task to protect standard-out.

- Task L2.3 : In method Intersection::addVehicleToQueue and in Vehicle::drive() ensure that the text output locks the console as a shared resource. Use the mutex _mtxCout you have added to the base class TrafficObject in the previous task. Make sure that in between the two calls to std::cout at the beginning and at the end of addVehicleToQueue the lock is not held.

Dependencies:
-   OpenCV 

How to run this project:

    root@a9ad274128c4:/home/workspace/L3_Project# mkdir build
    root@a9ad274128c4:/home/workspace/L3_Project# cd build
    root@a9ad274128c4:/home/workspace/L3_Project/build# cmake ..
    root@a9ad274128c4:/home/workspace/L3_Project/build# make
    root@a9ad274128c4:/home/workspace/L3_Project/build# ./traffic_simulation
