# habitat_multi_docker
Install docker-ce and then install the NVIDIA Container Toolkit using this link:
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html

Finally, run these commands to clone this repo and build an image:

```bash
cd ~
git clone https://github.com/UMich-CURLY/habitat_multi_docker.git
cd habitat_multi_docker
sudo docker build --tag dockerv1 .
```

Run the bash file as follows:

```bash
cd habitat_multi_docker/
sudo chmod +x launch_docker.sh
sudo ./launch docker.sh
```
  
  Inside your docker container, you will find that all the associated code it in the right path.
  
  Namely we have two repositories in our docker path:
  
  1. tour_mathing_routing
  2. habitat_ros_interface

  Moreover there are 2 conda environments in your docker environment. 
  1. habitat - Based in python3.7 and runs all the files related to habitat_sim and habitat_lab
  2. robostackenv - Based in python3.9 and runs everything in ros noetic
 
  Once you're in your docker continure to run the following statements 
  
  4. cd ~/catkin_ws
  5. catkin_make - to built packages
  6. source devel/setup.bash
