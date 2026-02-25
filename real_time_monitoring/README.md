cd stress_ws
colcon build --packages-select stress_inference_pkg
source install/setup.bash

t1: ros2 run stress_inference_pkg stress_inference_realtime

t2: ros2 run stress_inference_pkg mock_publisher
t2: ros2 run stress_inference_pkg emobit_publisher

t3: ros2 topic pub /user_feedback std_msgs/msg/String "data: 'stressed'" --once

To launch the emobit oscilloscope: run_emotibit
