
To build:
```
dts devel build -f --arch arm32v7 -H <HOSTNAME>.local
```

To launch on duckiebot:
```
docker -H <HOSTNAME>.local run --name rescue-acquisition-bridge --rm --network=host -v /data:/data -e LAB_ROS_MASTER_IP=<LAB_SERVER_IP> -dit duckietown/rescue-acquisition-bridge:daffy-arm32v7
```

To launch the acquisition bridge on a watchtower : 

```
docker -H <HOSTNAME>.local run --name rescue-acquisition-bridge --rm --network=host -dit -e LAB_ROS_MASTER_IP=<LAB_SERVER_IP> -e ROBOT_TYPE=watchtower duckietown/rescue-acquisition-bridge:daffy-arm32v7
```
