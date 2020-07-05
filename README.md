# ork-simulations
Repository to host OpenRocket simulations

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
