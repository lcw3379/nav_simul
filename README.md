네비게이션 툴박스를 gazebo + rviz환경에서 구동하기 위한 연습환경 제작.

구동 모델은 기본 터틀봇 모델을 사용한다.

기본 터틀봇 월드 환경에서 구동해보면서 어떤 노드와 토픽들이 사용되는지, 어떤 글로벌/로컬 플래닝 알고리즘이 사용되는지, 각 알고리즘마다 필요한 설정(yaml)에는 어떤 게 있는지 알아보는 시간을 가진다.




1번째 터미널에

ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py

2번째 터미널에

ros2 launch nav2_bringup bringup_launch.py use_sim_time:=true autostart:=true map:=/home/user_name/my_map.yaml

3번째 터미널에

ros2 run rviz2 rviz2 -d $(ros2 pkg prefix nav2_bringup)/share/nav2_bringup/rviz/nav2_default_view.rviz



![map1](https://github.com/user-attachments/assets/daf72f01-4578-4499-b40c-565aafd5bea8)



로봇 근처와 경로에 생기는 화살표는 지능로봇 강의시간 때 들은 거 같은데... 잘 기억이 나지 않는다.

이제 어떤 알고리즘이 사용되는지, 무슨 설정을 해야 하는지, 직접 만든 로봇엔 어떨게 nav2를 적용해야 하는지 알아야 하겠다.




1. nav2

![image](https://github.com/user-attachments/assets/d05d9496-eacf-4f89-9a5a-49d5c483718f)



