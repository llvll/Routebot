# Routebot
##Trajectory data mining from GoPro videos using Visual SLAM and Visual Odometry.

I've started working on a project about the trajectory data mining from videos - for example: snowboarding video from GoPro action camera.

This is the continuation of my previous experiment (MotionML), which was based on the accelerometer datasets and KNN-DTW classification: [https://github.com/llvll/motionml](https://github.com/llvll/motionml)

Visual odometry and monocular SLAM topics have been researched with the following algorithms:

1. PTAM
2. DTAM
3. LSD-SLAM
4. ORB-SLAM

At this stage I've selected **ORB-SLAM** algorithm for the initial experiments: [https://github.com/raulmur/ORB_SLAM2](https://github.com/raulmur/ORB_SLAM2)

The implementation of Routebot is done in C++ and Python using Scikit-Learn and FastDTW for the model training purposes based on the trajectory data. The data mining itself, based on OpenCV and ORB-SLAM, will execute on Apache Spark for video file processing.

The following results are expected:

1. Extracted trajectory data.
2. Discovered and classified motion patterns - similar to MotionML project above.
3. Video georeferencing or spatio-temporal referencing - GPS geotagging might be present for frame #1, trajectory data will extrapolate geotagging to the next frames. Clock synchronization should take place.

IPython Notebook (.ipynb file) is included for step-by-step execution of the demo application with extra comments.

Please feel free to ask any questions: oleg.v.puzanov@gmail.com
