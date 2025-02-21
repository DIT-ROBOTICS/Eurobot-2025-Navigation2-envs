# Eurobot-2025-Navigation2-envs
The Docker Environment of ROS2 Humble for Eurobot-2025-Navigation2

## One-Line Command To Run

On 11, run mode
```
docker compose -f /home/navigation/Eurobot-2025-machine-ws/src/Eurobot-2025-Navigation2-envs/Navigation2-humble-deploy//docker-compose.yaml run --rm navigation-run-11
```
On 12, run mode
```
docker compose -f /home/navigation/Eurobot-2025-machine-ws/src/Eurobot-2025-Navigation2-envs/Navigation2-humble-deploy//docker-compose.yaml run --rm navigation-run-12
```

On R2-11, develop mode
```
docker compose -f /home/navigation/Eurobot-2025-machine-ws/src/Eurobot-2025-Navigation2-envs/Navigation2-humble-deploy//docker-compose.yaml run --rm navigation-develop-11
```
On R2-12, develop mode
```
docker compose -f /home/navigation/Eurobot-2025-machine-ws/src/Eurobot-2025-Navigation2-envs/Navigation2-humble-deploy//docker-compose.yaml run --rm navigation-develop-12
```

On Local, develop mode
```
docker compose -f /home/navigation/Eurobot-2025-machine-ws/src/Eurobot-2025-Navigation2-envs/Navigation2-humble-deploy//docker-compose.yaml run --rm navigation-develop-local
```

On Local, RViz mode
```
docker compose -f /home/tars3017/Documents/DIT/Eurobot-2024-Local-ws/src/Eurobot-2024-Navigation-Main/Eurobot-2024-Navigation-envs/deploy/docker_deploy.yaml run --rm navigation-rviz-11
```

```
docker compose -f /home/tars3017/Documents/DIT/Eurobot-2024-Local-ws/src/Eurobot-2024-Navigation-Main/Eurobot-2024-Navigation-envs/deploy/docker_deploy.yaml run --rm navigation-rviz-12
```

## ------------ Basic commands ------------

## Start Container
```
docker compose -f "path to compose file/compose file name" up -d
```

## Attach Container
```
docker exec -it "container name" bash
```

## Launching Navigation2
### Simulation On Local Machine - open rviz & navigation with odometry simulation
```
ros2 launch navigation2_run sim_launch.py
```
### Run On Real Machine - open navigation with listening to the topic /final_pose from localization
```
# on remote machine
ros2 launch navigation2_run real_launch.py 

# on local machine
ros2 launch navigation2_run rviz_launch.py
```
