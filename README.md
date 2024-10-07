# Acomm Drivers
This is ros2 package stack to interface with acoustic beacons (e.g., USBL, Modem). In the future, it may have more ros driver for other type acoustic beacons. 

## Installation:

### install goby dependency: [reference](https://goby.software/3.0/)
```sh
# To install release packages on Ubuntu
$ echo "deb http://packages.gobysoft.org/ubuntu/release/ `lsb_release -c -s`/" | sudo tee /etc/apt/sources.list.d/gobysoft_release.list
$ sudo apt-key adv --recv-key --keyserver keyserver.ubuntu.com 19478082E2F8D3FE
$ sudo apt update
# minimal
sudo apt install libgoby3-dev goby3-apps
# full
sudo apt install libgoby3-dev libgoby3-gui-dev goby3-apps goby3-gui goby3-doc goby3-test libgoby3-moos-dev goby3-moos
```

### ros2 build:
```sh
$ cd /Your_Workspace/src
$ git clone -b humble-devel https://github.com/GSO-soslab/acomm_drivers
$ cd acomm_drivers
$ git submodule update --init --recursive
$ cd /Your_Workspace/src
$ colcon build --packages-select acomms_msgs evologics_ros
# or
$ colcon build
```

### Usage:
```sh
$ cd /Your_Workspace/
$ source ~/Your_Worksapce/install/setup.bash
$ ros2 launch evologics_ros start.launch.py
```

### Basic introduction (todo...):
<pre>

structure:
    |___ acomms_msgs: the customter ros2 message for the acomm stack
    |___ evologics_ros: the ros2 driver to talk with evologics USBL or modem.
    |___ seatrac_ros: todo...

</pre>