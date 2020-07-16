# ork-simulations
Repository to host OpenRocket simulations

### Directory
[Installing OpenRocket](##installation)
[Design Reference](##design-reference)

## Installation

### Ubuntu/Debian
The command ```sudo apt-get install openrocket``` does not work. To run OpenRocket, you will have to download the ```.jar``` file and execute it using Java 8. Increasingly, debian distros default with Java 8+, so you'll have to install Java 8 first. 

1. Install Java 8
```
sudo apt install openjdk-8-jdk
```

1. Check for Java 8 Path (hacky method, don't actually update your preference). Take note of path
```
sudo update-alternatives --config java
```

1. Make a directory to store OpenRocket
```
cd ~ && mkdir OpenRocket
```

1. Download the OpenRocket 15.03 .jar file
```
wget https://github.com/openrocket/openrocket/releases/download/release-15.03/OpenRocket-15.03.jar -O ~/OpenRocket/OpenRocket-15.03.jar
```

1. Set OpenRocket to executable
```
cd ~/OpenRocket && chmod +x OpenRocket-15.03.jar
```

1. Run OpenRocket
```
<path_to_java_8> -jar ~/OpenRocket/OpenRocket-15.03.jar
```

## Design Reference

The goal is to design a dual-deployment rocket with roughly the following stages. In our case, we will be swapping the locations of the main chute and the drogue chute. 

Generally, the order of the rocket should be as follows

1. Nose cone
1. Payload
1. Main Chute
1. Electronics Bay
1. Drogue Chute
1. Propulsion & Fins

Keeping the payload in the front allows for placing the center of mass to be towards the front of the rocket. Our goal is to keep the center of mass ahead of the center of pressure for the rocket (or else it won't fly). 

Keeping the electronics bay in between the parachutes makes it easier for the flight computer to ignite both switches (shorter wires, less chance of failure, etc).

![west-rocketry-reference](http://westrocketry.com/articles/DualDeploy/dual.jpg)
