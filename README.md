
2. Open a terminal within the environment.
3. Navigate to the `src` directory of your workspace using:
   ```sh
   cd ~/catkin_ws/src
   ```

### Step 4: Create the Robot Arm Package
1. Create a new package for your robot arm:
   ```sh
   catkin_create_pkg my_robot_arm std_msgs sensor_msgs roscpp
   ```
2. Navigate to the newly created package directory:
   ```sh
   cd my_robot_arm
   ```

### Step 5: Define the Robot Description
1. Create a URDF file for your robot arm in the `urdf` directory:
   ```sh
   mkdir urdf
   cd urdf
   touch my_robot_arm.urdf
   ```
<img width="959" alt="1" src="https://github.com/user-attachments/assets/b0d1a262-832a-4b31-a466-a7ea2373ba19">
   
2. Open the `my_robot_arm.urdf` file and define the URDF for your robot arm.

<img width="947" alt="2" src="https://github.com/user-attachments/assets/7835911d-bfb2-493b-95ff-bc41bf024bf3">

### Step 6: Add Dependencies
1. Open the `package.xml` file and add necessary dependencies for your robot arm package, such as `roscpp`, `std_msgs`, `sensor_msgs`, and any other relevant packages.

<img width="947" alt="3" src="https://github.com/user-attachments/assets/78c5a792-6d7f-4a7a-91a9-6b2033b18a80">

### Step 7: Create Launch Files
1. Create a `launch` directory:
   ```sh
   mkdir launch
   cd launch
   touch display.launch
   ```
<img width="443" alt="4" src="https://github.com/user-attachments/assets/78b87885-1e0a-4740-ad97-7203e4d81995">
   
2. Open `display.launch` and add the launch file code to launch your robot arm in RViz.

<img width="949" alt="5" src="https://github.com/user-attachments/assets/fd2c00cd-ca45-4997-9780-1df1ea45610c">

### Step 8: Write Nodes for Controlling the Robot Arm
1. Create a `src` directory:
   ```sh
   mkdir src
   cd src
   touch robot_arm_controller.cpp
   ```
2. Write your ROS node code in `robot_arm_controller.cpp` to control the robot arm.

![image](https://github.com/user-attachments/assets/8d9a3a34-cb31-4a8e-ab13-5b4bdd229b45)
   

### Step 9: Build the Package
1. Go back to the root of your workspace:
   ```sh
   cd ~/catkin_ws
   ```
2. Build your package:
   ```sh
   catkin_make
   ```
   
3. Source the setup file:
   ```sh
   source devel/setup.bash
   ```

### Step 10: Launch the Robot Arm in RViz
1. Use the launch file to start your robot arm in RViz:
   ```sh
   roslaunch my_robot_arm display.launch
   ```
<img width="946" alt="7" src="https://github.com/user-attachments/assets/3325e0f5-23d0-435f-a7c7-540d7648e800">
<img width="946" alt="9" src="https://github.com/user-attachments/assets/05613a56-4fa9-4cae-a2b9-394bbd793ce5">
<img width="944" alt="10" src="https://github.com/user-attachments/assets/72e567d8-3bf2-42c5-b404-c392b820b593">
