
# Target pursuit


## Description

We make the drone to move towards a tagged target. The drone does not have a camera, so we use the laptop's camera.
The laptop takes a picture of the environment, detects the marker and then instructs the drone to fly to the target.


## Material/Equipment

- Laptop with a camera
- CoDrone
- Marker (April tag)

![](https://www.cnet.com/a/img/j8Jyt-UNj36WrvLbVWnXU1WawPw=/470x353/2016/01/08/bd231247-8b12-4d2a-bfe2-98f210c3c48b/byrobot-dfx-battle-drone.jpg)

<img src="https://repository-images.githubusercontent.com/285867695/dc81c800-dd4b-11ea-9b11-4ec97fb40565" width=200></img>


## Software

- CoDrone Python module
- April tag detector


### Program to detect the position of the marker



### Program that instructs the drone to fly to the target


<img src="images/robolink.jpeg" width=200></img>

'''
  0 import CoDrone
  1 from CoDrone import Direction
  2
  3 drone = CoDrone.CoDrone()
  4 drone.pair( drone.Nearest )
  5
  6 drone.turn(Direction.LEFT,2,80)
  7 drone.turn(Direction.RIGHT,2,80)
  8 drone.land()

'''



### Demo [Video]















