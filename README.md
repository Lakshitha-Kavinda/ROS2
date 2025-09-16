# ROS2
ROS 2 basics and example projects

- Creating a package
  ```shell
  ros2 pkg create --build-type ament_python robokeeper_servo_driver
  ```
- Building an package
    colon buid
- Sourcing a package
  source install/setup.bash
- running a package
   ros2 run robokeeper_servo_driver servo_driver

- Making a python script executable
  chmod +x src/robokeeper_servo_driver/robokeeper_servo_driver/servo_driver.py
  

- The entry_points tells ROS2 which Python function to run. Your servo_driver.py must have a main() function. And added into setup.py
    ex: 'servo_driver = robokeeper_servo_driver.servo_driver:main',
- Publishing an angle to a topic
    ex: ros2 topic pub /servo_angle std_msgs/msg/Int32 "data: 45"
